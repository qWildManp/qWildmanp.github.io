+++
date = "2023-09-30"
title = "Level Design: Redesign of Dishonored Level"
draft = false
image = "img/portfolio/Work5/title_img.png"
showonlyimage = false
weight = 1
+++
**Introduction**: It is a 3-week personal Level Design project inpired by the Level "Dishonorned" in Dishonored 1. Use Unreal 5 as Game Engine and Level UP toolkit as Level Editor 




<!--more-->


{{< figure
  src="img/portfolio/Work5/title_img.png"
  type="full"
  width="50%"
  label="Level Overview"
  caption="Level Map - Layout" 
>}}

#### Finish Date: Nov 2023
#### Project Length : 2 weeks

## Video Walkthrough
{{< youtube XF5XtHUYSlU>}}

## Playable Demo

### [Level Demo v1.3  {{< ico "bxs-file-archive" "boxicons">}}](https://drive.google.com/file/d/11jugzxy9sQlOLNlqdizve3TD8uA7szrY/view?usp=drive_link "Level Demo")

## Level Narrative Intro
Similar to Dishonred 1 ,player was a prisoner who was locked in royal secret prison in a desolute island .One day a mysterious force suddenly attacked the prison . You got a chance to escape from the prosion.

## Level Overview

The expected time of the whole level experience would be 10 minutes ,each approach will be around 5 minutes.Player will experience 3 sublevel areas: “Special Prison”,”Central Prison” and “Prison Exit”. Players will start from “Special Prison” and finish the level at “Prison Entrance”. Each sublevel experience time would be 2 - 3 minutes. In this level, player will learn the interaction of **“Climb” ,”Jump”,”Interaction with button”,”Use of pole”,”Hide in Cover” and ”Danger of Security Camera”**. 



## Level Design - Pre-production

#### Learning the Limits
I use [Level UP Level Design Toolkit](https://projects.etc.cmu.edu/level-up/ "Level UP Tookkit") as my Level Editing toolkit，so I first dig into how far that this toolkit can do to learn about the limitations in my level design. I played its playground scene where they show up all the features that this package is capable of. After test runing, without writing any script I notice following limitations of this toolkit :
1. No Enemy AI
2. Button switch with limited usage -- Only can triger Door
3. Objects cannot block the view of Camera



#### Metrics Mesurements

Size of the space is cutial in level design.Before I start to draw somthing on paper. I first take a measurement of Unreal Unit Cube which can be helpful for me to manage level size. I simply opened a sample third person scene and tried randomly build a room to mesure the character size ,and I test the relative feeling of object size with different scales cubes. After the measurement, I go bakc to my grid paper and set 1 grid stands for 3 Unreal Unit length.
{{< gallery >}}
{{< figure
  src="/img/portfolio/Work5/Metrics.png"
  width="40%"
  label="matrics"
  caption="Character size in Unreal" 
  >}}
{{< figure
  src="/img/portfolio/Work5/Metrics2.png"
  width="40%"
  label="matrics"
  caption="Build room and objects using cubes with unit grid material" 
  >}}
  {{< figure
  src="/img/portfolio/Work5/Metrics3.png"
  width="40%"
  label="matrics"
  caption="Paper Design based on metrics" 
  >}}
{{< /gallery >}}

#### Paper Designs

I planed my brain-storming of the level by playing the "Dishonored" Level - Escape from prison phase many times . I tried to extract the fun aspects and level pacing during that period. I noticed that the most interesting part when I was playing the level was player can have more than one path to reach the goal.In the prison escape phase, it had three main moments (excape from the cell and avoid guards --> stole the bomb in a room --> Go the exit ,plant the bomb and break out the exit door) and it offers at least 2 times during the whole prison escape experience. 

{{< figure
  src="/img/portfolio/Work5/level_overview.jpg"
  type="full"
  width="40%"
  label="Level Overview"
  caption="Level Map - Layout" 
  >}}

  This is the rough arrangment of the level. Getting inspired by the prison escape in the "Dishonored" Level, I divided my level into three sections. Each section have different emphasis and have two solutions that to pass the section. Considering on the limitation of the toolkit,which is no enemy will walk around the level , so I shift the sneaking experience from encounter-battling to more like puzzle-solving.


{{< table "table table-striped table-hover" >}}
|**Level Section**| 1.Specal Prison  | 2.Central Prison | 3.Prison Entrance
|---------|---------|--------|--------|
|**Expected Experience**\ **Difficulty**|Intimate Space,Guided,Teaching \ Tutorial Level     |Prospect Space,High Intensity dodging / jumpiing\  Chanllenging Level   | Prospect Space,Moderate Intensity dodging / jumping,Puzzle Solving \ Challenging Level
|**Major Obstacles** | Path A: Door Puzzle, Pole Puzzle      | Path A: Moving Cameras(Danger Zone)   | Path A: Moving Pattern of two cameras
|                    | Path B: Static Platforms | Path B: Moving Platforms          | Path B: Moving Pattern of one camera, Pole Puzzle
{{</ table >}}

Key Experience and Obstacles in sublevels

{{< gallery >}}
{{< figure
  src="/img/portfolio/Work5/legend_1.jpg"
  caption="Level Map - Lengend" 
  label="Level Overview"
>}}
{{< figure
  src="/img/portfolio/Work5/legend_2.jpg"
  label="Level Overview"
  caption="Level Map - Lengend" 
  >}}
{{< /gallery >}}

List of legends to ensure the consistency of level objects

{{< gallery 
  hover-effect="grow" 
  dir="/img/portfolio/Work5/Paper Designs" />}}{{< load-photoswipe >}}

Detailed paper design of each level section(room)


## Level Design - In-production

#### Greyboxing

Because the level is devided in 3 sections, I build the level by sections. Firstly, I only built walls and vertical space of each section based on papaer design, and playtest myself in the space.Then I will make some tweaks of space size if the space is too large or narrow.
{{< gallery >}}
{{< figure
  src="/img/portfolio/Work5/Sublevel1_greybox.jpg"
  caption="Sublevel1 - greybox" 
  label="Level Overview"
>}}
{{< figure
  src="/img/portfolio/Work5/Sublevel2_greybox.jpg"
  caption="Sublevel2 - greybox" 
  label="Level Overview"
>}}
{{< figure
  src="/img/portfolio/Work5/Sublevel3_greybox.jpg"
  caption="Sublevel3 - greybox" 
  label="Level Overview"
>}}
{{< /gallery >}}

Secondly, when space is decieded, interative objects and major guidance will be added into the level

{{< gallery  hover-effect="grow" 
  dir="/img/portfolio/Work5/Detailed GreyBox" />}}

#### Redesign of Sublevel 2

#### Playtesting and Iterations

## Screen Shots

{{< figure
  src="/img/portfolio/Work5/GameFlow.jpg"
  label="Level Overview"
  caption="Level Flow - Finalized blockmesh" 
>}}



[1]:/img/portfolio/Work5/title_img.png