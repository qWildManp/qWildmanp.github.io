+++
date = "2022-10-21"
title = "Procedual Generate Level: Deadly Game"
draft = false
image = "/img/portfolio/Work1/LevelGeneratePrototype.png"
showonlyimage = false
weight = 1
+++

<!--more-->
It is a procedural generated map tech approach


## Procedual Level Gnertator
{{< figure
  src="/img/portfolio/Work1/LevelGeneratePrototype.png"
  type="full"
  label="LevelGenerate"
  caption="Level Generation-Prototype" >}}
 {{< figure
  src="/img/portfolio/Work1/LevelGenerateFinal.png"
  type="full"
  label="LevelGenerate"
  caption="Level Generation-Final" >}}


### Basic Approach
Procedural generated map. the number of rooms in each sub-level is certain, but the selection and arrangement of room types are randomly distributed. I use scriptable file to store the room requirements of each sub-level. The generation process uses scriptable to traverse each sublevel one by one to ensure that the sublevels are generated in order.

### Problem Solving

#### Overlaping Issue



[1]:/img/portfolio/Work1/Work1_title.png