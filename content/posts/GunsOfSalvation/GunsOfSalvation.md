+++
date = '2025-05-03T10:35:33-06:00'
draft = false
title = 'Guns of Salvation'
+++
![main](/JustinTAlexander-AWebsite/images/GOStext.png)

# Description
*Guns of Salvation* is a 2.5D Metroidvania set in the realm of Lleh. It follows Iris and her journey to defeat the Seven Deadly Sins and free the cherubs trapped around the realm. It was developed using Unreal Engine 5.4.

I was brought on to this project to design and implement the three boss fights that are featured in its spring demo: Sloth, Gluttony, and Wrath. This involved frequent meetings with the team's leads, weekly progress reports, and coherent design documentation.  

# Credits
Developed by a team of ~15 peers as a student capstone project.

On this project, I am credited as:
- Programmer (Unreal Blueprints)
- Game Designer (Boss fights)

# Design
## State Machine
My primary contribution to *Guns of Salvation* took the form of a state machine that all boss enemies inherit.

This machine alternates between the "Idle" and "Attacking" states. In the latter, a random attack function (0, X) is called and executes to completion. Then, the Idle state is triggered, which functions as a buffer between attacks.

The number of available attack functions and the time spent in between them both depend on what phase the boss is currently in. Each child of the parent boss actor is responsible for determining what the conditions for incrementing this phase are, and they have the option of not doing so at all.

Once the boss's health drops to 0, the Idle/Attacking loop is broken and the "Death" state is entered. This triggers one-time logic in which (typically) the boss actor is destroyed and reward items are spawned for the player to collect.
