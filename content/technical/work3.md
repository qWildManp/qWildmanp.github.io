+++
date = "2023-02-15"
title = "Traditional Animation : Inverse Kenematic"
draft = false
image = "img/portfolio/TechWork3/Title.png"
showonlyimage = false
weight = 1
math = true
+++

**Introduction**: C++ implmentation of inverse kenematic 
<!--more-->
 {{< figure
  src="/img/portfolio/TechWork3/Jacobian.gif"
  type="full"
  label=""
  caption="Procedual Animation using Jacobian Approach" >}}

### Goal
Implement two procedural animation techniques (CCD and Transpose Jacobian)
Compare results between two methods


### Technique - CCD
Cyclic Coordinate Descent Inverse Kinematics

##### Main idea:  
align one joint with the end effector and the target at a time, so that the last bone of the chain iteratively gets closer to the target.

##### Algorithm:

{{< highlight Shell "linenos=table" >}}
Target T (x_t,y_t);
End Effecter E (x_e,y_e);
Joint J(x_j,y_j)
dis(T,E)
WHILE(dis(T,E) is not close enough)
DO
		
		Vector3 normalized(JT);
		Vector3 normalized(JE);
		Quat q = Compute rotation quaternion 	from JE -> JT;
		apply quaternion rotation to current joint J;
		Update new dis(T,E);
		IF current J is root joint
		DO
			reset to first joint;
		ELSE
			change current J to upper joint;
		END IF	
		dis(T,E)
END WHILE
{{< /highlight >}}

##### Video:
{{< youtube hXf7ExYrs6c>}}


### Technique – Jacobian Transpose IK(3DOF)(Numerical Approach)

##### Main idea : Jacobian Matrix
 ### $ 𝐽∆ \theta= ∆𝑒 $
 ### $ 𝐽^{−1}𝐽∆ \theta = 𝐽^{−1}∆𝑒 $
 ### $ ∆ \theta= 𝐽^{−1}∆𝑒 => 𝐽^T∆𝑒 $


##### Algorithm:

{{< highlight Shell "linenos=table" >}}
Target T (x_t,y_t);
End Effecter E (x_e,y_e);
Joint J(x_j,y_j)
dis(T,E)
dynamic scaler Alpha
matrix delta_theta(9, 1);	

matrix delta_e(3, 1);
delta_e.setValue(dis(T,E).x, 0);
delta_e.setValue(dis(T,E).y, 1);
delta_e.setValue(dis(T,E).z, 2);

WHILE(dis(T,E) is not close enough)
DO
	previous_dis = dis(T,E)
	Matrix jacobian[3][3*num_of_joint];

	//set small push to rotate arm
	FOR int j = 0 ;j < num_of_joint ;j++
	DO
		FOR int axis = 0; axis < 3; axis ++
		DO
			quat step = compute a step rotation quaternion based on axis;
			Character::tmp_pose;
			copy current arm rotation into tmp_pose;
			apply rotation to tmp_pose;
			Vector 3f delta_e_step = tmp_pose_joint[joint_idx] – current_pose[joint_idx];
			float delta = delta_e_step / step;
			jacobian[0][j*3 + axis] = delta.x;
			jacobian[1][j*3 + axis] = delta.y;
			jacobian[2][j*3 + axis] = delta.z;
		END FOR
	END FOR
	Compute Jacobian Transpose jacobian_T[3*n][3];
	Compute new delta_theta;
	Apply rotation to current pose by new delta_theta = Alpha * j_t * delta_e;
	dis(T,E)
	delta_e.setValue(dis(T,E), 0, 0);
	delta_e.setValue(dis(T,E), 1, 0);
	delta_e.setValue(dis(T,E), 2, 0);
	IF 
		dis(T,E)  <= previous_dis = dis(T,E)
	DO
		Alpha = Alpha * 7;
	ELSE IF
	 	dis(T,E)  > previous_dis = dis(T,E)
	DO
	   Alpha = Alpha / 7;
	END IF
END WHILE
{{< /highlight >}}

##### Video:
{{< youtube VT-blNPDEwI>}}

### Result Compare
1. CCD method moves faster than Jacobian IK
2. Jacobian IK is smoother than CCD
3. CCD will take more time to converge to best approximation

### Discussion
1. My version of Jacobian IK don’t seriously think of picking a good scalar value α
2. My Jacobian IK treats all joint with 3DOF
3. Thinking of trying more Jacobian option (like pseudo-Jacobian, Damped least squares)
4. Analytical Jacobian Method is hard to think when facing more than 1 DOF robotic arm









