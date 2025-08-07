+++
date = '2025-07-07T10:35:33-06:00'
draft = false
title = 'Snogbert'
+++
![main](/JustinTAlexander-AWebsite/images/SnogbertMain.png)

# Description
"Legends tell of a die named Snogbert...
Does he have infinite sides, or only one?"

*Snogbert* is a 2D platformer with characteristics of the roguelike/roguelite and arcade genres. It stars Snogbert–a mythical infinite-sided die–and his quest to return home after falling into a cave network inhabited by other sentient dice. 

The game features a “die roll” system that randomly assigns the criteria to complete each level. So, while a similar set of levels is traversed with each run, players are encouraged to think about them differently every time. 

# Timeline
Development on *Snogbert* was paused after the release of the 1 Year of Snogbert demo in January 2024.
Find the 1 Year of Snogbert demo on itch.io: [https://mrstarman18.itch.io/snogbert-demo] (https://mrstarman18.itch.io/snogbert-demo)

In April 2025, I presented the project at Lipscomb University's Imagine House pitch competition and was one of 3 finalists selected to receive funding. This went toward a Steam release for the full game.
Find *Snogbert* on Steam: [https://store.steampowered.com/app/3742030/Snogbert/] (https://store.steampowered.com/app/3742030/Snogbert/)

# Credits
Developed by Justin T. Alexander, with music and some game design by Noah Hudson-Camack.

On this project, I am credited as:
- Game Designer
- Programmer (C++, UE5 blueprint code)
- Musician
- Character Designer
- Story Author
- Artist

# Design
## Gameplay
*Snogbert*'s gameplay loop is designed to create replayability through unpredictability. This is largely achieved via the "die roll" missions--the randomly-assigned criteria to complete each level. These missions add onto the random level order to keep players on their toes, and they require players to fully explore both their moveset and their surroundings. 

Towards this end, the first 6 missions Snogbert encounters are as distinct from one another as possible. For instance, a player's gameplay for *Stay in the Air* and *Jump Limit* missions would be nearly opposite of one another, as would their gameplay for *K.O. Enemies* and *Avoid Enemies*. 

As the game progresses, more missions are introduced as well. These are designed in one of two ways:
1) Highlight new additions such as enemy types and interactible objects. For instance, World 2's *Break the Targets* features the new D8 enemy and Target object.
2) Challenge players to master their moveset. For instance, World 2's *Run.* features a Shadow enemy that follows the player's movements exactly.  

## Level Design
*Snogbert*'s one-room levels largely serve as playgrounds for the random missions, further encouraging players to explore the best ways to accomplish their goals. My primary goals in designing them were 1) that they feel good to move around in for players and 2) they're traversible by the game's enemies (minimizing "dead zones").

The following is an example of early level designs, which were done using the game's tilesets to measure Player and Enemy movement along a more precise grid. This approach allowed me to guarantee that levels could be navigated regardless of skill level, so it was primarily used for World 1.
![BB](/JustinTAlexander-AWebsite/images/BB_LevelDesign10.png)

As development progressed and character's movement came to be more understood, level concepts were able to be sketched by hand and then implemented directly in-engine. This approach focused on capturing what a level should feel like to traverse, which granted more design freedom. The following are examples of such levels from Worlds 2 and 3.
![CC](/JustinTAlexander-AWebsite/images/CC_DesignPostits.png)
![DD](/JustinTAlexander-AWebsite/images/DD_LevelDesign3.PNG)

![ItsTime](/JustinTAlexander-AWebsite/images/TimeToGetSnoggy.png)
