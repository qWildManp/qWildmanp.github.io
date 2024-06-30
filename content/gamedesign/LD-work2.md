+++
date = "2023-09-30"
title = "Level Design - RPG: Iron Fortress"
draft = false
image = "img/portfolio/LD-work2/title_img.png"
showonlyimage = false
weight = 2
+++
**Introduction**: It is a 4-week personal Level Design project inpired by "DarkSouls" and "Elden Ring". Use Unreal 5 as Game Engine and Level UP toolkit as Level Editor 


<!--more-->


{{< figure
  src="img/portfolio/LD-work2/overview.png"
  type="full"
  width="70%"
  label="Level Overview"
  caption="" 

>}}

#### Finish Date: Nov 2023
#### Project Length : 3 weeks

## Video Walkthrough
{{< youtube GiXK0TSc2Fs>}}

## Playable Demo

### [Level Demo v0.3  {{< ico "bxs-file-archive" "boxicons">}}](https://drive.google.com/file/d/12KUJVFCiiD3ES6Hb79ozxXPnVnWbnNfO/view?usp=drive_link "Level Demo")

## Level Narrative Intro
The player wakes up at an altar on an nameless mountain with a message in mind : Go to the Iron Fortress, and kill the Iron Lord and regain the power you have. Then the player start the journey towards Iron Fortress.
## Level Overview

The expected time of the whole level experience would be 20-30 minutes .Player will able to explore 4 areas: “Nameless Mountain”,”Fortress Periphery
” ,“Outer Fortress” and "Inner Fortress". Players will start from “Nameless Mountain” and finish the level at “Inner Fortress”.  In this level, player will learn the interaction of **“Move” ,”Jump”,”Battling with enemy”,"Solve Puzzle",”Use of Firebomb”**. 



## Level Design - Pre-production

#### Metrics Mesurements

Because of my [First Level Design Project]( {{< ref "/gamedesign/ld-work1" >}} "LD-Work 1"), I 'm more familar with the unit size of Unreal Engine. However, different from my first Level Design Project, this project has a larger level map and also it should include some non-linear areas. So, during my paper design process, I use simple cubes to create some areas to measure the space and feeling.
{{< gallery >}}
{{< figure
  src="/img/portfolio/LD-work2/metric_1.png"
  width="40%"
  label="matrics"
  caption="General Space Messurement" 
  >}}
{{< figure
  src="/img/portfolio/LD-work2/metric_2.png"
  width="40%"
  label="matrics"
  caption="Use of standard UE character mesh as reference" 
  >}}
  {{< figure
  src="/img/portfolio/LD-work2/metric_3.png"
  width="40%"
  label="matrics"
  caption="Creating space of fortress area" 
  >}}
  {{< figure
  src="/img/portfolio/LD-work2/metric_4.png"
  width="40%"
  label="matrics"
  caption="Adding more rooms and mesuring room sizes" 
  >}}
{{< /gallery >}}

#### Paper Design

I 'm a big fan of FormSoftware, and I played many Soul-like games, which gives me some preknowlege about how "Soul-like" level is composed of. The key is : **"One clear main path/loop, bended with multiple side paths/loops in the map"**. Besides, I decide to watch some level runthrough videos and search for some level breakdowns of "Souls-like" games. Theses resource helped me a lot on the knowledge of  builing structure , connections between rooms/space and creating loops in the level. After necessary research, I decided to design a fortress level which I think is more manageable considering of the time limit of the proejct.

{{< figure
  src="/img/portfolio/LD-work2/levelLayout.png"
  type="full"
  width="50%"
  label="Level Overview"
  caption="Level Map - Layout" 
  >}}
  
{{< figure
  src="/img/portfolio/LD-work2/levelLayout-heightMap.png"
  type="full"
  width="50%"
  label="Level Overview"
  caption="Level Map - Layout Height Map" 
  >}}

  This is the topdown layout(interier space no included) of the level. I divided my level into four sections. Each section has its key experienece(as shown in below table). At each section, there are some optional areas for player to explore,reasonable rewards will be given if the player finish expolring those areas.

{{< table "table table-striped table-hover w-auto" >}}
|**Level Section**| 1.Nameless Mountain  | 2.Fortress Periphery | 3.Outer Fortress | 4. Inner Fortress
|---------|---------|--------|--------|---------|
|**Expected Experience**\ **Difficulty**|Basic Tutorial, Exploration,Low intensity encounters |Level mechanics Tutorial(**Firebomb**), Exploration,Moderate intensity encounters,Puzzle-solving encounter| Repeat & practice of level mechanics, High intensityencounters, Puzzling solving encounters | Advanced usage of level mechanics, Puzzle solving,moderate intensity encounters,Boss Fight |
|**Major Obstacles** | Normal Enemy      | Normal Enemy, Armored Enemy   | Normal Enemy, Armored Enemy, Elite Armored Enemy, One-side Door | Normal Enemy, Armored Enemy, Puzzle, Boss, One-side Door
{{</ table >}}

Key Experience and Obstacles in each area

{{< gallery >}}
{{< figure
  src="/img/portfolio/LD-work2/levelLegend.jpg"
  caption="Level Map - Lengend" 
  label="Level Overview"
>}}

{{< /gallery >}}

List of legends to ensure the consistency of level objects

{{< gallery 
  hover-effect="grow" 
  dir="/img/portfolio/LD-work2/Paper Designs" />}}{{< load-photoswipe >}}

Detailed paper design of each level area

#### Mood Board
During paper design, I made a mood board as an architectural reference and art reference for my level layout. Also the mood board help me to mesure current level flow and how each key moment are placed in the map.

{{< figure
  src="/img/portfolio/LD-work2/mood board.png"
  caption="Level Mood Board" 
  label="Level Mood Board"
>}}

[Mood Board Link ](https://miro.com/app/board/uXjVNU-1o5I=/ "Mood Board")

## Level Design - In-production

#### Greyboxing

In this project, part of greyboxing are doing during my paper design process, which is a more efficient in-production process. Because main experience happens in the fortress, I decide to build fortress level and its surrounding areas first, then build the mountain level. My approach in this process is : 
1. Using simple cubes to create general space of level map.
2. Based on decided space, using simple walls to create rooms and divide sub areas; Add some placeholders as enemies
3. Adjust walls' height based on height map, adjust some walls/cubes to fit the design perpose; Resise some areas if it's too large/narrow
{{< gallery 
  hover-effect="grow" 
  dir="/img/portfolio/LD-work2/Grey Boxing" />}}{{< load-photoswipe >}}

#### Level Mechanics Implementation
In this project, I implement three major level mechaincs :
1. Throwing Firebomb

{{< figure
  src="/img/portfolio/LD-work2/fireBomb.gif"
  caption="" 
  label="Level Mechanics"
>}}


Blueprint:

{{< figure
  src="/img/portfolio/LD-work2/throwFirebomb_blueprint.png"
  width="50%"
  caption="" 
  label="Level Mechanics"
>}}

2. Powder Keg
   
{{< figure
  src="/img/portfolio/LD-work2/powderKeg.gif"
  caption="" 
  label="Level Mechanics"
>}}

Blueprint:

{{< figure
  src="/img/portfolio/LD-work2/powderKeg_blueprint.png"
  width="50%"
  caption="" 
  label="Level Mechanics"
>}}

3. Puzzle Elevator
   
{{< figure
  src="/img/portfolio/LD-work2/elevator.gif"
  caption="" 
  label="Level Mechanics"
>}}

Blueprint:

{{< figure
  src="/img/portfolio/LD-work2/puzzleElevator_blueprint.png"
  width="50%"
  caption="" 
  label="Level Mechanics"
>}}

#### Iterations and Playtesting

 After the grey-boxing, I add interative objects into the level : puzzles, collectable objects and enemies. Not all the level mechanics are implemented at the same stage of time, so I will use some cheap placeholders/implements at first and then gradually replace them with actual featrue.  After that, I add some neccessary art assests and lights in my level to enrich the environment narritive,  and use different colors of material to set the color tone of each part of the level.
  
{{< gallery >}}
{{< figure
  src="/img/portfolio/LD-work2/addingDetail_1.png"
  caption="Adding detail - Two Tower -1F" 
  label="Level Overview"
>}}

{{< figure
  src="/img/portfolio/LD-work2/addingDetail_2.png"
  caption="Adding detail - Watch Tower" 
  label="Level Overview"
>}}

{{< figure
  src="/img/portfolio/LD-work2/addingDetail_3.png"
  caption="Adding detail - Fortress Area" 
  label="Level Overview"
>}}

{{< figure
  src="/img/portfolio/LD-work2/addingDetail_4.png"
  caption="Adding detail - Mountain Cave" 
  label="Level Overview"
>}}

{{< figure
  src="/img/portfolio/LD-work2/addingDetail_5.png"
  caption="Adding detail - Outer Fortress" 
  label="Level Overview"
>}}

{{< figure
  src="/img/portfolio/LD-work2/addingDetail_6.png"
  caption="Adding detail - Two Tower 2F" 
  label="Level Overview"
>}}

{{< /gallery >}}


 During the production process I got my playtested with some of my schoolmates and friends. They provides me some valuable insights that helps me to make my level better. Here are some examples during the playtest-iteration process :

**1. Playtester did not notice how to open the front gate shortcut**
   
  Issue noticed :
  1. Weak connection between the front gate and open switch ：The path from gate to switch is long and no guidance to show the connection
  2. Player dont think the front gate is locked
  3. When player trigger the gate switch, there is no noticable feekback.


  Change:
  1. Make some holes that the player can see the gate from above
  2. using more noticable color to draw connection between gate and the switch
  3. When player openup the door, provide sound effect and visual feedbacks

  {{< figure
  src="/img/portfolio/LD-work2/iteration_1.png"
  caption="" 
  label="iteration"
>}}

**2. Confusion point at outer fortress**

  Issue noticed :
  1. Player cannot notice that the left path is the exit of the other path and right path is the path he should go
  2. If player mistakenly choose the wrong path, player will be easy to get lost in this section

  Change:
  1. Seperate two path : Now the player will not easy to notice the other path at this point
  2. Using enemy to attract player's attention
  3. Using broken fence as a soft blockout and leading lines to guide player not shift to a wrong path

  {{< figure
  src="/img/portfolio/LD-work2/iteration_2.png"
  caption="" 
  label="iteration"
  >}}


**3. 2F of Watch tower is too narrow** 

  Issue noticed :
  1. The entrance of 2F is too narrow and angles are too limit to player , which makes the player intend not to approach the 2F and stuck
  2. Covers are too far away from player to approach and hide
  3. Enemy are too centralized ,player will be easy to just sneak through the , not use firebomb to pass this area

  Change:
  1. Create a another path that let player can reach the 2F and also stand in a vantage point
  2. Make cover more avaliable to player
  3. Make enemy less centralized , let player throw firebomb from top to down : make stealth experience more reasonable


 {{< figure
  src="/img/portfolio/LD-work2/iteration_3.png"
  caption="" 
  label="iteration"
  >}}


 

## Screen Shots
{{< gallery-slider dir="/img/portfolio/LD-work2/ScreeShots/"  width="1000px" height="500px" auto-slide="2000" >}}

## Documentation
{{< gdocs src="https://docs.google.com/viewer?srcid=1YtA_ZZapUZY-D7VPwa-iMjl6_X12u7XP&pid=explorer&efh=false&a=v&chrome=false&embedded=true" >}}

[1]:/img/portfolio/LD-work2/title_img.png