+++
date = "2024-2-30"
title = "Game Design - Puzzle Game: Cubic Factory"
draft = false
image = "img/portfolio/GD-Work2/GD-work2TitleImg.png"
showonlyimage = false
weight = 1
+++
**Introduction**: It is a 3D puzzle game on PC.
Core mechanic are boxing pushing and item interaction in the game . Player will play as a mouse sneak into the factory to steal the golden cheese.

<!--more-->
{{< figure
  src="img/portfolio//GD-Work2/GD-work2TitleImg.png"
  type="full"
  width="70%"
  label="Level Overview"
  caption="" 
>}}

Team members : 
Langxuan(Harry) He , Tingyu(Polly) Yan , Jiachen(Jason) Qiu , Yichen Lu , YuMeng(Meng) Wei

I'm the Level Designer/Co-Game Designer and Programmer in the team.

#### Finish Date: May 2024
#### Project Length : 2 month

## Game Overview
**Core Mechanics :**\
Box-pushing puzzle game, player will need to push objects in the level to clear the way/ trigger level mechanism\
**Basic Movement:**\
W - Forward\
A- Left\
S - Backward\
D - Right\
Space(Hold) - Push/Pull
## Video Walkthrough
{{< youtube iZaZp5wbpbY>}}
## Playable Demo
### [Cubic Factory v1.0  {{< ico "bxs-file-archive" "boxicons">}}](https://drive.google.com/file/d/15R7o-XaQ1GTrDYSuLYxwxKQXlBw8MMLt/view?usp=sharing "Game Demo")

## Game Design

In this game , me and my another Designer : Yichen are thinking of using the idea of **Emergent Design Patternt** in our puzzle game experience. We thought the Emergent Design patern can make the game have depth in gameplay with simple interactions. The player will be more likely have a experience of : using tools to solve the problem, not providing an question and wait for the player to fill the blank. Due to the time limit, we focus on one core mechanic : **Electricity**

#### Core Mechanic : Electricity

**Conductive**
* Circuit/Wires\
    Wires are the commonly noticed and widly used conductive object in our game. Wires are "connecters" and not movable. When wires are connected and create a circuit , it can be used to get trigger and conductive item to be electrified.
* Conductive Item\
    Conductive item is a more complex conductive object. It can be push/pull by the player. When it get close to the wire, it will be electrified and become a "connecter".However, when the conductive item is electrified, it will not be movable. This is a item both act as a tool and an obstacle, so player need to make a proper decision on moving these items. In this game demo , we use metal can as example.\
{{< figure
  src="/img/portfolio/GD-Work2/ConductiveItem.gif"
  type="full"
  label="Game Mechanic"
  caption="Conductive item : Wire and Metal can" >}}

**PowerSource**
* Battery
  Battery are the source to provide electricity. When it is on the power stand, it will start to electrify connected wires

  {{< figure
  src="/img/portfolio/GD-Work2/Battery.gif"
  type="full"
  label="Game Mechanic"
  caption="Power Source : Battery" >}}

**Trigger**
* Power stand : Place to contain battery
 {{< figure
  src="/img/portfolio/GD-Work2/Powerstand.png"
  type="full"
  width="40%"
  label="Game Mechanic">}}
* Button : Switch to activate/deactivate machines/doors
  {{< figure
  src="/img/portfolio/GD-Work2/Trigger.png"
  type="full"
  width="40%"
  label="Game Mechanic">}}
* Conveyor Belt : Conveyiny cubes in the game
  {{< figure
  src="/img/portfolio/GD-Work2/Conveyor.gif"
  type="full"
  width="40%"
  label="Game Mechanic">}}
* Door : Door that needs electricity
  {{< figure
  src="/img/portfolio/GD-Work2/Door.png"
  type="full"
  width="40%"
  label="Game Mechanic">}}


#### Core Mechanic : Electricity
  
## Level Design




