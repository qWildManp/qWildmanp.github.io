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

* Power stand\
  The place to contain battery. The start point of the circuit. In order not to make player confuse about electricity direction , we add power stand as a start point of the circuit. Electricity will start from the power stand.
 {{< figure
  src="/img/portfolio/GD-Work2/Powerstand.png"
  type="full"
  width="50%"
  label="Game Mechanic">}}
* Circuit/Wires\
    Wires are the commonly noticed and widly used conductive object in our game. Wires are "connecters" and not movable. When wires are connected and create a circuit , it can be used to get trigger and conductive item to be electrified. Wires are directional(180 degree and 90 degree), electriciy will only be conveyed along the circuit path.
* Conductive Item\
    Conductive item is a more complex conductive object. It can be push/pull by the player. When it get close to the wire, it will be electrified and become a "connecter". Different from the wire, conductive objects do not have directional property, it will electrify every conductives nearby . And, when the conductive item is electrified, it will not be movable. This is a item both act as a tool and an obstacle, so player need to make a proper decision on moving these items. In this game demo , we use metal can as example.\
{{< figure
  src="/img/portfolio/GD-Work2/ConductiveItem.gif"
  type="full"
   width="50%"
  label="Game Mechanic"
  caption="Conductive item : Wire and Metal can" >}}

**PowerSource**
* Battery\
  Battery are the source to provide electricity. When it is on the power stand, it will start to electrify connected wires
  {{< figure
  src="/img/portfolio/GD-Work2/Battery.gif"
  type="full"
   width="50%"
  label="Game Mechanic"
  caption="Power Source : Battery" >}}

**Trigger**

* Button : Switch to activate/deactivate machines/doors
  {{< figure
  src="/img/portfolio/GD-Work2/Trigger.png"
  type="full"
  width="50%"
  label="Game Mechanic">}}
* Conveyor Belt : Conveyiny cubes in the game
  {{< figure
  src="/img/portfolio/GD-Work2/Conveyor.gif"
  type="full"
  width="50%"
  label="Game Mechanic">}}
* Door : Door that needs electricity
  {{< figure
  src="/img/portfolio/GD-Work2/Door.png"
  type="full"
  width="50%"
  label="Game Mechanic">}}


#### Relationships between items : Electricity
The graph below shows how our features that relates to **Electricity** work with each other
   {{< figure
  src="/img/portfolio/GD-Work2/ElectricityRelationships.png"
  type="full"
  width="70%"
  label="Game Mechanic">}}

#### Other Game Features

**Game Camera Design**

The game Camera is in topdown view with the angle of 50 degree downwards from above and in fix distance. This camera angle can maximize the sptatial characteristics of 3D games and also give enough information for player to obtain.\
For some occlusion problems that still occur, we design a fixed camera rotation feature.Players can press **“Q”** to rotate clock-wise and **“E”** to rotate counter-clock-wise in 90 degrees. This allows players to better observe areas on the map that are obscured by objects.
{{< figure
  src="/img/portfolio/GD-Work2/CameraDesign.gif"
  type="full"
  width="70%"
  label="Game Mechanic">}}

**Asset Design**

To let player easy to measure the grid space in the level, we do some design in art asset.
1. We make a floor unit as same size as a grid unit and outline edges of a floor unit. Help player to have knowlege of our grid-based interactions and the size of each grid in our game
{{< figure
  src="/img/portfolio/GD-Work2/FloorSize.jpg"
  type="full"
  width="50%"
  label="Game Mechanic">}}
2. Make all interactable items tobe cube-like and no more than a size of a unit grid cube. Place all items at the center of the grid. 


## Level Design




