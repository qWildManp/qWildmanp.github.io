+++
date = "2022-12-10"
title = "Unreal VR Project : Lost in the Light"
draft = false
image = "img/portfolio/Work6/title_img.jpg"
showonlyimage = false
weight = 1
+++
**Introduction**: It is a 3-month coop project between ETC and Game For Change 2023. Create a transformational XR experience for the Games for Change festival held in New York City.

Team members:
Langxuan (Harry) He, Anlan Yang, Jessica Cromp, Jiaxin Li,Kailai Feng(Kai),Weixin Feng(Targy)

I am a gameplay programmer and a level designer in this project

<!--more-->

{{< figure
  src="img/portfolio/Work6/title_img.jpg"
  type="full"
  width="70%"
  label=""
  caption="" 

>}}

Finish Date: May 2023
## Video Demo
{{< youtube Ptwg27AP-E8>}}
## Game Overview
It's a flying simulation experience. Player will act as a songbird who is on a migration path starting from south to north. Because of the light pollution, player need to avoid those harmful light to not get disoriented in the game

**Keywords: Flying Simulation, Story Telling**

## Automatic flying system using Bezier Curve

 ### Basic Approach

 This project requires player to have a certain moving path throughout the experience, to simulate the reality bird migration path, I think using Bezier Curve to simulate the path is a good choice. I use the fomular of 5-point bezier curve to create the curve, because more control points can make curve more variant.

 {{< figure
  src="img/portfolio/Work6/bazier_curve.jpg"
  type="full"
  width="70%"
  label=""
  caption="" 

>}}


Compute a cureve based on control points
{{< highlight Shell "linenos=table" >}}
FVector AComputerBezier::ComputeBezierCurvePoint(TArray<FVector> pt_set,float t_value) {
	FVector P0 = pt_set[0];
	FVector P1 = pt_set[1];
	FVector P2 = pt_set[2];
	FVector P3 = pt_set[3];
	FVector P4 = pt_set[4];

	return  pow(1 - t_value, 4) * P0 
		+ 4 * pow(1 - t_value, 3) * t_value * P1 
		+ 6 * pow(1 - t_value, 2) * pow(t_value, 2) * P2 
		+ 4 * (1 - t_value) * pow(t_value, 3) * P3 
		+ pow(t_value, 4) * P4;
}
{{< /highlight >}}


Given a set of control points compute full flying path
{{< highlight Shell "linenos=table" >}}
void AComputerBezier::Tick(float DeltaTime)
{

	Super::Tick(DeltaTime);
	if (controlPts.IsEmpty())
		return;
	int ptStartIdx = ptSet_idx * 4;

	int numOfControlPts = GetNumOfControlPtsRemain(ptStartIdx);
	//get num of control points in front
	//there are enough number of control points and it is valid to insert new control point, so insert new set of control point
	if (numOfControlPts >= 5) {
		computeSet.Empty();
		for (int j = ptStartIdx; j < ptStartIdx + 5;j++) {
				computeSet.Add(controlPts[j]->GetActorLocation());
		}
		
	}
	else if (numOfControlPts < 5) {// it means there is not enough control point in front, so just stop 
		if(!for_test){
			reach_end_set = true;
		}
		else {
			ptSet_idx = 0;
		}
	}
	if (!reach_end_set) {// if current is not the end set keep calculate Bezier Curve point
		ComputeBezierCurvePoint();
	}
	if (t >= 1) {
		t = 0;
		ptSet_idx += 1;
		can_insert_new_pts = true;
	}
}
{{< /highlight >}}

### Resolve the sharp turnning point between two curve

 During the development , we found the if the gradient of the end of first curve and start of second curve is different, it will cause the "sharp turnning point"(shown as below), which will let player feel a sudden pause / turn at these edge points .To solve the sharp turning point issue, I try with a method to smooth it.
 {{< figure
  src="img/portfolio/Work6/sharp_turnning_point.jpg"
  type="full"
  width="70%"
  label=""
  caption="Sharp turning point between two single curves" 
>}}

 My approach is create a smoothing curve which will sampling five new control points from for example curve C1 and curve C2. They are p2' , p3 , p4 , p5 and p6'. The new points can create a "smoothing curve" (The purple curve).

  {{< figure
  src="img/portfolio/Work6/smoothing_curve.jpg"
  type="full"
  width="70%"
  label=""
  caption="Smoothing curve" 
>}}

  Then a blending attribute alpha is introduced to do the smoothing using follwing fomula :
  {{< figure
  src="img/portfolio/Work6/smooth_fomula.jpg"
  width="70%"
  label="Level Overview"
  caption="" 
 >}} 
 
 , Then we can smoothly blend two single Bezier Curves.

 {{< figure
  src="img/portfolio/Work6/final_curve.jpg"
  width="70%"
  label="Level Overview"
  caption="" 
 >}} 

 {{< highlight Shell "linenos=table" >}}

void AComputerBezier::SmoothingCurvePoint() {
	if (smoothingSet.IsEmpty()) {// if need to add new smoothing set
		float nextSetIdx = (ptSet_idx + 1) * 4;//start idx of next set
		if (GetNumOfControlPtsRemain(nextSetIdx)<5) {//there are no enough

			return;
		}
		else {
			for (int j = nextSetIdx; j < nextSetIdx + 5;j++) {
				nextComputeSet.Add(controlPts[j]->GetActorLocation());
			}
			smoothingSet.Add(ComputeBezierCurvePoint(computeSet, 0.5));
			smoothingSet.Add(computeSet[3]);
			smoothingSet.Add(computeSet[4]);
			smoothingSet.Add(nextComputeSet[1]);
			smoothingSet.Add(ComputeBezierCurvePoint(nextComputeSet, 0.5));
		}
		
	}

	// compute curve point on smoothing set
	FVector intersetCurvePt = ComputeBezierCurvePoint(smoothingSet, t_interset);
	
	//blend smoothing curve and current curve with smooth alpha
	FVector newcurvePt = (1 - smooth_alpha) * curvePt + smooth_alpha * intersetCurvePt;
	curvePt = newcurvePt;
	//updating smoothing alpha
	
	if (!freez_alpha) {
		t_interset += t_step * GetWorld()->GetDeltaSeconds();
		smooth_alpha += alpha_step * GetWorld()->GetDeltaSeconds();
		if (smooth_alpha > 0.9) {
		smooth_alpha = 0.9;
		}
		if (t >= 1){
			alpha_step = -alpha_step;
		}
		if (smooth_alpha < 0) {
		smooth_alpha = 0;

		alpha_step = -alpha_step;
		}
	}
	
	// if t_interset reach the end , its time change to another smoothing set of points
	if (t_interset >= 1) {
		t_interset = 0;
		smoothingSet.Empty();
		nextComputeSet.Empty();
	  }
  }
{{< /highlight >}}