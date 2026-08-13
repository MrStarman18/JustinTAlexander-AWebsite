+++
date = '2026-08-12T10:35:33-06:00'
draft = true
title = 'Michael Shane Neals Wardrobe'
+++
![main](/JustinTAlexander-AWebsite/images/vidogam.png)

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
# Inventory Management
The largest hurdle for this project was creating a system for inventory management, indexing, and storage to file that would remain scalable through a number of planned post-launch content updates.

I utilized the Unreal-native Data Tables and Structs to store information that remains constant at runtime (such as a list of all available clothing items).

This information is kept as lightweight Structs until an event occurs that transfers it onto a corresponding in-game actor (such as the player "equipping" a clothing item). Internally, this event causes existing actor's to change to that of the new item Struct rather than creating a new actor from scratch.

In this way, *Neal's Wardrobe* maintains the exact number of active actors that it needs at any given time without the risk of performance issues from spawning/despawning them. New items, events, and more are able to be added seamlessly by any team member by simply modifying the respective Data Tables.

![headshot](/JustinTAlexander-AWebsite/images/BuffWizardGame.png)
