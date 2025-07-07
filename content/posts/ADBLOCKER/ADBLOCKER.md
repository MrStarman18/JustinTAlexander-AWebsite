+++
date = '2025-06-19T10:35:33-06:00'
draft = false
title = 'AD BLOCKER: An Action Puzzle Game'
+++
![main](/JustinTAlexander-AWebsite/images/MainCapsule.PNG)
# Description
*AD BLOCKER* is a fast-paced match-3 puzzler that’s built for head-to-head gameplay between 0-2 players. It was developed using Godot Engine 4 and released to Steam on 2/28/2025.

*AD BLOCKER* features grid-based gravity and a unique linear garbage system. With a low skill floor and high skill ceiling, everyone will be able to play at their own pace. So whether you’re new to the action puzzle scene or a long-time genre fan of games like *Panel de Pon* and *TETRIS*, *AD BLOCKER* has something for you!

AD BLOCKER: An Action Puzzle Game was released on Steam on 2/28/2025.
Find it on Steam: [https://store.steampowered.com/app/3187360/AD_BLOCKER_An_Action_Puzzle_Game/](https://store.steampowered.com/app/3187360/AD_BLOCKER_An_Action_Puzzle_Game/)

# Credits
Developed by Justin T. Alexander, with art by William McKelvey and other contributions from several peers and friends.

On this project, I am credited as:
- Game Designer
- Programmer (C#)
- Musician
- Character Designer
- Story Author
- Artist
as well as managing the game's two rounds of playtesting and its social media presence (under my personal account @/MrStarman18).

# Design
## Gameplay
![MatchEntity](/JustinTAlexander-AWebsite/images/ADBLOCKER_MatchEntityDiagram.jpg)
Each match of *AD BLOCKER* revolves around the two player boards and their interactions with one another. The BoardManager class oversees this. In addition to tracking overarching values such as game speed and selected characters, it also passes signals such as input and incoming garbage down to each Board. However, to the BoardManager, a Board is a black box.

The Board class tracks the state of the player grid, especially the locations and statuses of each Block therein. When it receives signals from the Board Manager, it handles interactions with the Block(s) and Cursor objects that are associated with it.

The following is an early concept for how Blocks travel between the two Boards, later dubbed "Linear Garbage".
![BlockConcept](/JustinTAlexander-AWebsite/images/ADBLOCKER_BlockMovementConcept.gif)

## CPU Player
![CPU](/JustinTAlexander-AWebsite/images/ADBLOCKER_CPUFlowDiagram.jpg)
As advertised, *AD BLOCKER* is playable by 0-2 players and heavily features a single-player Story Mode. Thus, a computer player that could provide both challenge and fairness was needed. We decided that such a CPU should have the following goals:
- Make swaps that are worth more points (gain score)
- Make swaps that keep its board from overflowing (survive)

The first goal is achieved using a priority queue that ranks all swaps available. A swap is scored based on the location that each of its two Blocks will be in afterward; that is, looking ahead to account for gravity.

The CPU's second goal of survival is achieved in two ways. First, a swap's priority increases the further away it is from the Board's center. Second, when a Block enters the furthest two spaces from the Board's center, any swap that brings it closer is immediately made top priority. Both solutions outrank any score-based match that would've been at the head of the queue, simulating the sense of urgency that a real player would experience.

## Menu UI
![MenuFlow](/JustinTAlexander-AWebsite/images/ADBLOCKER_MenuFlowDiagram.jpg)
*AD BLOCKER*'s menus aim to replicate the simplicity of similar arcade titles, striking the balance between a stylized experience and one that takes the shortest amount of time to start a game.

# Postmortem (authored 6/2025)
This past semester, I had my first experiences successfully deploying software projects as a team lead. Today, I offer a retrospective on AD BLOCKER: An Action Puzzle Game, which I released to Steam on 2/28/2025 and am currently providing bugfixes for as issues are reported.

We began active development in February 2024 as a team of three with the goal of finishing the game in a year. One year later, we met this goal as a team of two (myself and an artist), with one contract SFX author.

AD BLOCKER was a fully indie project, with the narrative and asset direction stemming from a premise I'd long held onto ("A game show where the contestants are based on commercials!"). From a gameplay approach, we wanted to create a puzzle game that's optimized for head-to-head gameplay by maximizing how the players' actions affect one another. 
Toward this end, the earliest element we designed as a team was its "Linear Garbage" system, which contrasted garbage systems in many other genre entries (internally called "Exponential Garbage"). This choice and its consequences led to many other unique features of AD BLOCKER, such as its stricter adhesion to grid-based movement, its center hold area being shared by both players, and its time measurement being explicitly in ticks rather than seconds. 

From a marketing perspective, the game was a lesson on highlighting these unique elements. I won't deny that there are several similar games for sale, many of which also pull inspiration from Tetris Attack. Our design took pains to make AD BLOCKER unlike its competitors, but the challenge came with presenting why any of these differences would be tangibly valuable to a player. 

On the other hand, a marketing win came from my organization of the Action Puzzle Bundle, a collaborative Steam bundle between our game and 4 others in the same genre. This allowed me to speak with like-minded developers, both those who had long been established and those who were releasing as close as weeks before we were.

At a personal level, AD BLOCKER is something near to me. I consider it a testament to all I've learned about game design and the balance between creativity and scope. With only self-imposed deadlines to keep us accountable, I'm proud of what we were able to produce.

Ultimately, I'm happy to have been able to stay with the project from concept to release. While design decisions were made as a team, I feel that my personal touch is uniquely present in every aspect of AD BLOCKER's identity. I was there when we decided on its colorful TV aesthetic, its funk-inspired sound, the voices and motivations for each character, the logic behind its CPU players, and everything in between. The experience was one I won't soon forget.

![lib](/JustinTAlexander-AWebsite/images/LibraryCapsule.PNG)
