+++
date = "2022-10-21"
title = "Unity 3D Horror Game: Deadly Game"
draft = false
image = "img/portfolio/Work1/Work1_title.png"
showonlyimage = false
weight = 3
+++

**Introduction**: PC, First person single player horror game, playing as a white-collar worker who was caught by killer at 6:06 am one day. Without any special skills and strength, player need depend on himself to solve puzzles in each level of the house and escape from killer.
<!--more-->
![gamelogo][1]

Finish Date: Nov 2021

It is an 2 month personal Project
## Video Demo
{{< youtube lB5ub4J4oaU >}}
## Game Overview

The core gameplay is puzzle solving with element of roguelike , survive.The main theme is realistic horror. Player will act as a poor victim who was thrown into a mistery house, player need to explore the dim room, get rid of killer’s pursue and finally find out the exit of the house and escape.

**Keywords: Horror,Puzzle Game**
## Overview of Levels

#### Level Flow

{{< figure
  src="/img/portfolio/Work1/LevelGeneratePrototype.png"
  type="full"
  label="LevelGenerate"
  caption="Level Generation-Prototype" >}}


**First Level - intro level** : Player Start Room , one exploring room and one danger room.

**Second Level - danger level** : two exploring rooms and three danger rooms

**Third Level - puzzle level** :  two puzzle rooms, two exploring rooms and two danger rooms

#### Item
 {{< figure
  src="/img/portfolio/Work1/item.png"
  type="full"
  label="item"
  caption="Random Generated Item" >}}

The random generation of items adopts the method of arranging generation points. The items required by each sub level will be randomly generated at the generation points. The items required by each sub level and the corresponding number of items are also stored through scriptable. After the room is generated, the objects are randomly generated.

## Puzzle Design
**Statue (Color hint)**
 {{< figure
  src="/img/portfolio/Work1/StatuePuzzle.png"
  type="full"
  height="85%"
  width="85%"
  label="Statue Puzzle"
  caption="Statue Puzzle(Color Hint) Game Scene Picture" >}}

This is a room with 6 statues. Players need to push the statue to the correct position according to the orientation of the statue and the color hint of the light

**Statue (Paper hint)**
 {{< figure
  src="/img/portfolio/Work1/StatuePuzzle2.png"
  type="full"
  height="85%"
  width="85%"
  label="Find missing part"
  caption="Statue Puzzle(Paper Hint) Game Scene Picture" >}}

There are three animal statues in the exhibition hall. Players need to find clues and place the animal statues in the correct position according to the clues(Clues will be randomly generated).

**Find Missing Part**
 {{< figure
  src="/img/portfolio/Work1/MissingPart.png"
  type="full"
  height="85%"
  width="85%"
  label="Find missing part"
  caption="Find Missing Part Game Scene Picture" >}}

This is a locked parlor room. Players need to find the handle of the electric box and turn off the electric box to unlock the room

**Gravity Ball**
 {{< figure
  src="/img/portfolio/Work1/GravityPuzzle.png"
  type="full"
  height="85%"
  width="85%"
  label="Find missing part"
  caption="Gravity Puzzle Game Scene Picture" >}}

This is a puzzle of gravity maze. Players control the rolling of the ball by manipulating the chassis. Players need to move the ball from the starting point in the upper left corner to the end point in the lower right corner.

## Design WorkFlow
 {{< figure
  src="/img/portfolio/Work1/WorkFlow.png"
  type="full"
  label="Workflow Picture"
  caption="" >}}



[1]:/img/portfolio/Work1/Work1_title.png