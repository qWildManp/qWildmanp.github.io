+++
date = "2023-09-30"
title = "Level Design - Platformer Level : Saved by the Bell"
draft = false
image = "img/portfolio/LD-work1/title_img.png"
showonlyimage = false
weight = 2
+++
**Introduction**: It is a 3-week personal Level Design project to design a 3D platformer level. Use Unreal 5 as Game Engine and Level UP toolkit as Level Editor 




<!--more-->


{{< figure
  src="img/portfolio/LD-work1/title_img.png"
  type="full"
  width="70%"
  label="Level Overview"
  caption="" 

>}}

#### Finish Date: Nov 2023
#### Project Length : 2 weeks

## Video Walkthrough
{{< youtube XF5XtHUYSlU>}}
backup link ： https://pan.baidu.com/s/1ZexGNDlcxZiu6sbDod4EvA?pwd=amje

## Playable Demo

### [Level Demo v1.3  {{< ico "bxs-file-archive" "boxicons">}}](https://drive.google.com/file/d/11jugzxy9sQlOLNlqdizve3TD8uA7szrY/view?usp=drive_link "Level Demo")
backup link : https://pan.baidu.com/s/1E-nGAcoEIY6uzTX67Qy8nw?pwd=dg3s

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
  src="/img/portfolio/LD-work1/Metrics.png"
  width="40%"
  label="matrics"
  caption="Character size in Unreal" 
  >}}
{{< figure
  src="/img/portfolio/LD-work1/Metrics2.png"
  width="40%"
  label="matrics"
  caption="Build room and objects using cubes with unit grid material" 
  >}}
  {{< figure
  src="/img/portfolio/LD-work1/Metrics3.png"
  width="40%"
  label="matrics"
  caption="Paper Design based on metrics" 
  >}}
{{< /gallery >}}

#### Paper Design

I planed my brain-storming of the level by playing the "Dishonored" Level - Escape from prison phase many times . I tried to extract the fun aspects and level pacing during that period. I noticed that the most interesting part when I was playing the level was player can have more than one path to reach the goal.In the prison escape phase, it had three main moments (excape from the cell and avoid guards --> stole the bomb in a room --> Go the exit ,plant the bomb and break out the exit door) and it offers at least 2 times during the whole prison escape experience. 

{{< figure
  src="/img/portfolio/LD-work1/level_overview.jpg"
  type="full"
  width="50%"
  label="Level Overview"
  caption="Level Map - Layout" 
  >}}

  This is the rough arrangment of the level. Getting inspired by the prison escape in the "Dishonored" Level, I divided my level into three sections. Each section have different emphasis and have two solutions that to pass the section. Considering on the limitation of the toolkit,which is no enemy will walk around the level , so I shift the sneaking experience from encounter-battling to more like puzzle-solving.


{{< table "table table-striped table-hover w-auto" >}}
|**Level Section**| 1.Specal Prison  | 2.Central Prison | 3.Prison Entrance
|---------|---------|--------|--------|
|**Expected Experience**\ **Difficulty**|Intimate Space,Guided,Teaching \ Tutorial Level     |Prospect Space,High Intensity dodging / jumpiing\  Chanllenging Level   | Prospect Space,Moderate Intensity dodging / jumping,Puzzle Solving \ Challenging Level
|**Major Obstacles** | Path A: Door Puzzle, Pole Puzzle      | Path A: Rotating Cameras (Danger Zone)   | Path A: Moving Pattern of two cameras
|                    | Path B: Static Platforms | Path B: Moving Cameras          | Path B: Moving Pattern of one camera, Pole Puzzle
{{</ table >}}

Key Experience and Obstacles in sublevels

{{< gallery >}}
{{< figure
  src="/img/portfolio/LD-work1/legend_1.jpg"
  caption="Level Map - Lengend" 
  label="Level Overview"
>}}
{{< figure
  src="/img/portfolio/LD-work1/legend_2.jpg"
  label="Level Overview"
  caption="Level Map - Lengend" 
  >}}
{{< /gallery >}}

List of legends to ensure the consistency of level objects

{{< gallery 
  hover-effect="grow" 
  dir="/img/portfolio/LD-work1/Paper Designs" />}}{{< load-photoswipe >}}

Detailed paper design of each level section(room)


## Level Design - In-production

#### Greyboxing

Because the level is devided in 3 sections, I build the level by sections. Firstly, I only built walls and vertical space of each section based on papaer design, and playtest myself in the space.Then I will make some tweaks of space size if the space is too large or narrow. Then jumping platforms ,doors ,secret holes will be added in to test if they are accessable/jumpable.
{{< gallery >}}
{{< figure
  src="/img/portfolio/LD-work1/Sublevel1_greybox.jpg"
  caption="Sublevel1 - greybox" 
  label="Level Overview"
>}}
{{< figure
  src="/img/portfolio/LD-work1/Sublevel2_greybox.jpg"
  caption="Sublevel2 - greybox" 
  label="Level Overview"
>}}
{{< figure
  src="/img/portfolio/LD-work1/Sublevel3_greybox.jpg"
  caption="Sublevel3 - greybox" 
  label="Level Overview"
>}}
{{< /gallery >}}


#### Redesign of Sublevel 2

During the greyboxing process, I found the my original design of sublevel 2 is hard to implemented. Because "Dodging the camera using cover" is the key experience in this section, but "X-Ray Camera" will break the experience. This let me to reconsider the design of Sublevel 2. When rethinking of my design of Sublevel 2, In found following designed problems with my current design:

**1. The two level paths are not clear enough**
  
 {{< figure
  src="/img/portfolio/LD-work1/Issue_in_sublevel2.jpg"
  width="60%"
  label="Level Issue"
  caption="Two ways to finish the level are so close" 
>}}

Here is the comparison between two paths to finish this section. It is obvious that two paths are actually going along with only one path, the only difference is press the side button or not. I think this wil make player feel confused about different choices in level, or player may not notice there is two ways to pass this section.

**2. The experience of two approachs are too similar**
  
Another issue I noticed in my design in sublevel 2 is two paths hves similar playing experience. In design, the core experience is diffrerent for each path. One will more focus on player cautious playing style and environment observation, the other will be more focus on risky playing style and instant decision making (Detailed can bereferenced from documentation below).

Based on above issue, I redesigned the second section as following :
{{< figure
  src="/img/portfolio/LD-work1/Redesign_of_sublevel2.jpg"
  width="60%"
  label="Level Overview"
  caption="Redesign of sublevel 2 - redesign the level path" 
>}}

 In the new design, first thing I do is to sepreate two path to make each path unique to the player. I think this change can make the choice of path more clear to the player. Now one approach(On the left) to finish is at the first floor of the room ,and for the other approach(On the right), all experience will happen at second floor. Next, I redesign the experience of two paths. I keep the core playing experience of each path as baseline of this level section, and make my two paths more fit the experience. For the first path(on the left), in stead of "using cover to avoid camera's view", I change it to "Player need to observe the movng patterns of those security cameras", I add some safe zones(refer to the green areas in above figure) for player to stand/temperarily stand and think of the next step. For the second path(on the right), I change it from "camera dodging game" to "platformers", now the player won't experience any deadly cameras(they are at 1F), but the player need to make use of the cameras holders to jump through this section. These holders are always moving / rotating, which requires player to play more risky and make fast decisions in this path.

#### Iterations and Playtesting

 After the grey-boxing and finalize the design, I started to add more detailed in my scene, which are all interative objects and some main guidance to lead player. After that, I finished other building parts to enrich the environment narritive, and here comes to the first version of my level.
  
{{< figure
  src="/img/portfolio/LD-work1/level_v1.jpg"
  width="60%"
  label="Level Overview"
  caption="Blockmesh - version 1" 

>}}

 {{< gallery  hover-effect="grow" 
  dir="/img/portfolio/LD-work1/Detailed GreyBox" />}}

  After finishing the first version I got it playtested with someof my schoolmates and friends. They provides me some valuable insights that helps me to tweak my level better. Here are some examples during the playtest-iteration process :

**1. Exit of sublevel misguide player**
   
  Issue noticed :

  Some playtester are misguided in this section because of the direction of the door. Above figure shows that player should go left to exit this section, but the door direction blocks the view from the 
  left and suggest a wrong way ------ go to the exit of the other path and get lost.

  Change:

  1. Change the direction of the door to guide the player in a correct direction 
  2. Add another locked door at the exit of the other path to seperate two paths.

  {{< figure
  src="/img/portfolio/LD-work1/Iterate_1.jpg"
  label="Level Interate"
  caption="" 
  >}}

**2. Confusing at level section 2**

Issue noticed : 

 1. Some playtesters cannot notice there is another path and cannot distinguish the difficulties between two paths
 2. Some pipes outside of section 2 guide playtester out of playing area.
 3. Some playtesters feel confused about where to go when entered the level.

Change:
 1. At outside of section 2, add more visualize guidance (leading lines, contrast) and remove some unnessary pipes.

{{< figure
  src="/img/portfolio/LD-work1/Iterate_2_1.jpg"
  label="Level Interate"
  caption="" 
  >}}

 2. Move the checkpoint area (the entrance) of the section outside of room so that player will be able to see the entrance of each path earlier

{{< figure
  src="/img/portfolio/LD-work1/Iterate_2_2.jpg"
  label="Level Interate"
  caption="" 
  >}}

 3. Inside of section 2, break some walls to create a converging point to attract players attention

{{< figure
  src="/img/portfolio/LD-work1/Iterate_2_3.jpg"
  label="Level Interate"
  caption="" 
  >}}

**3. Hard for player to know the struacture of the level**

Issue noticed :

A playtester said my level is hard to get familiar with the whole level structure, just feel like following a sequence of room and reach the end.

Change:

It's a bit chanllenge issue for me, but I still tried some efforts to help player to know my level strcuture.

1. Make the exit of level be the landmark in the level and create some view points where player can find the landmark in different view. 
 
{{< figure
  src="/img/portfolio/LD-work1/Iterate_3_1.jpg"
  label="Level Interate"
  caption="" 
  >}}

2. Create some peek points for players to notice another possible path to make structural connections between different paths. 
{{< figure
  src="/img/portfolio/LD-work1/Iterate_3_2.jpg"
  label="Level Interate"
  caption="" 
  >}}

3. Using some building structures to reveal some hiden spaces to encourage player to explore the level.
{{< figure
  src="/img/portfolio/LD-work1/Iterate_3_3.jpg"
  label="Level Interate"
  caption="" 
  >}}

4. Rveal some information about incoming challenge to movtive player.
{{< figure
  src="/img/portfolio/LD-work1/Iterate_3_4.jpg"
  label="Level Interate"
  caption="" 
  >}}

## Screen Shots
{{< gallery-slider dir="/img/portfolio/LD-work1/ScreeShots/"  width="1000px" height="500px" auto-slide="2000" >}}

## Documentation

backup link : https://pan.baidu.com/s/1QIQ_gQ6-pGv1nj60b3FpQw?pwd=frgb

{{< gdocs src="https://docs.google.com/viewer?srcid=1OcROdeQtPJjOXnz7Ugb2YgmKKAR64E3I&pid=explorer&efh=false&a=v&chrome=false&embedded=true" >}}

[1]:/img/portfolio/LD-work1/title_img.png