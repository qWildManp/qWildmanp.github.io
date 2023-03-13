+++
date = "2022-10-22"
title = "Personal Project: Magic Thief"
draft = false
image = "img/portfolio/Work2/Work2_title.png"
showonlyimage = false
weight = 2
+++

**Introduction**: Once upon a time, there is a kingdom called Zauberlehr. It has a great knowledge of magic and Spells, but it has a strict hierarchy. Only nobles can have the access to magic, common people are forbidden to use or even learn magic. However, there is a good thief called Roger, who is smart and full of a sense of justice...


<!--more-->
![gamelogo][1]

Finish Date: Jan 2022
## Game Overview

In this game, the player will act as Magic Thief – Roger. Running through the magic kingdom, crossing layers of obstacles, escape from the royal knight’s chasing, and defeat bosses.

**Keywords: 2D plateformer**
## Gameplay Mechanics - Autorun
The look of players' automatic movement is achieved by movement of game map. Give the player initial speed and acceleration, and spped thredshold.While the player's speed is increasing, the game map will calculate tge relative movement speed and start moving.

## Level Design
#### Level1 - Tutorial Level
{{< figure
  src="/img/portfolio/Work2/Level1-blueprint.png"
  type="full"
  label="Level 1 - Tutorial Level"
  caption="Level 1 Blueprint" >}}
  {{< figure
  src="/img/portfolio/Work2/Level1-layout.png"
  type="full"
  label="Level 1 - Tutorial Level"
  caption="Level 1 Layout" >}}

  This Level is designed to be the tutorial level. In this level player will get to know basic control and special ability.Therefore, the level is focusing on easy jump,slide,spell..etc. In each area of level, the teaching-practice method is adopted to help players get familiar with the game.

#### Level2 - Boss Level(Endless Level Boss Fight)
{{< figure
  src="/img/portfolio/Work2/bossLevel-blueprint.png"
  type="full"
  label="Level 2 - Boss Level"
  caption="Level 2 Blueprint" >}}
{{< figure
  src="/img/portfolio/Work2/bossLevel-layout.png"
  type="full"
  label="Level 2 - Boss Level"
  caption="Level 2 Layout" >}}

  This level is to consolidate abd testing the understanding of existing mechanisms. Therefore, this level is divided into three sub-areas, and each sub-area focuses on challenging one of player's abilities. Area 1(jump),Area 2(fireball)and Area 3(Sliding).And the attack behaviour of boss is designed accordingly to what player has learnt in each subarea to fit the challenge.

#### Boss Design
**Boss Behavior**
{{< figure
  src="/img/portfolio/Work2/bossBehavior_code1.png"
  type="full"
  label="Boss Design"
  caption="Boss Attack Behavior" >}}
  {{< figure
  src="/img/portfolio/Work2/bossBehavior_code2.png"
  type="full"
  label="Boss Design"
  caption="Boss Attack Modes" >}}
  {{< figure
  src="/img/portfolio/Work2/bossBehavior_animationTree.png"
  type="full"
  label="Boss Design"
  caption="Boss Animation Tree" >}}
1. Motar shooting
2. Release Royal Knight(Enemy)
3. Cannon Fire

When the player in a specific sub-area, it will let the boss in one of the modes.When player switch from one sublevel to another, ther boss will also change its attack mode
## Video Demo
{{< youtube 4Xw11oWWrbE >}}


[1]:/img/portfolio/Work2/Work2_title.png