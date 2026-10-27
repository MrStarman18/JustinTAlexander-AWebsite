+++
date = '2026-08-12T10:35:33-06:00'
draft = false
title = 'Michael Shane Neals Wardrobe'
+++

# Description
*Michael Shane Neal's Wardrobe* is a mobile dress-up game in which players receive clothes via a gacha economy and use them to form outfits and compete in a number of events befitting a true gentleman. It was developed using Unreal Engine 5.8.

I was brought onto this project as the programming lead. As such, I was solely responsible for system design and implementation based on feature requests given by the project lead.
I was also heavily involved in gameplay design discussions, especially related to outfit scoring and the gacha economy.

# Credits
Developed by a team of ~6 in collaboration with the artist Michael Shane Neal, specifically his appearance on TikTok at @brushwithstyle.

On this project, I am credited as:
- Programmer (UE5 blueprint code)
- Game Designer

# Design
## Inventory Management
The largest hurdle for this project was creating a system for inventory management, indexing, and storage to file that would remain scalable through a number of planned post-launch content updates.

I utilized the Unreal-native Data Tables and Structs to store information that remains constant at runtime (such as a list of all available clothing items).

This information is kept as lightweight Structs until an event occurs that transfers it onto a corresponding in-game actor (such as the player "equipping" a clothing item). Internally, this event causes existing actor's Struct(s) to change into that of the new item Struct rather than creating a new actor from scratch.

In this way, *Neal's Wardrobe* maintains the exact number of active actors that it needs at any given time without the risk of performance issues from spawning/despawning them. New items, events, and more are able to be added seamlessly by any team member by simply modifying the respective Data Tables.

## Outfit Scoring
As I designed the event system for *Neal's Wardrobe*, a point of contention arose when deciding how to objectively score an outfit. There are many points that could be graded on, but which would resonate most with players' expectations and with the intended feel for this game? 
 
Our final system utilizes the following points on its scoring rubric:
- Style Stats: Every article of clothing has a positive or negative value for 6 stats (i.e. Formal, Modern, or Artistic). Most events will store 1-3 of these stats and determine the bulk of an item's score based on its values in the relevant categories. For instance, a Formal event rewards more points for clothing with a high Formal stat. This step ties into the game's overarching narrative focus on creating the right outfits for the right occasions, not just outfits that the player likes. About 1/2 of an outfit's score is determined here.
- Collection: Every article of clothing belongs to a Collection, an in-game method of grouping that simulates brand names and/or designer outfits. An outfit rewards a predetermined number of points based on how few unique Collections are present in it. The maximum number of points is given for 1-2 colors, then this amount decreases with each new Collection past 2. About 1/4 of an outfit's score is determined here.
- Color: Every article of clothing has 1-2 Colors, matching the colors seen when looking at it. An outfit rewards a predetermined number of points based on how few unique colors are present in it. The maximum number of points is given for 1-3 colors, then this amount decreases with each new color past 3. This step is meant to represent how a real-life outfit should match visually, regardless of where its pieces originate from. About 1/4 of an outfit's score is determined here.
- Rarity: Every article of clothing has a rarity from 1-5, indicating how likely it is to be randomly pulled from the gacha. Rarer items also give a small number of bonus points when worn in an outfit, serving as a scoring cushion for lucky (or persistent) players. These points can be added, but their abscense will never count against the player.

As players unlock more Clothing types, the score ceiling increases proportionally. Each category determines its maximum values based on the number of Clothing types the player has available, thus allowing the same set of events to scale in difficulty over time.

