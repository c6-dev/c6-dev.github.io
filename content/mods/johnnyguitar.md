+++
title = "JohnnyGuitar NVSE"
date = "2021-06-28"
author = "carxt, lStewieAl, c6"
cover = "img/jg/cover.jpeg"
description = "For the one they call Johnny Guitar..."
+++

JohnnyGuitar NVSE is an engine plugin for New Vegas that adds new script functions, features and bug fixes.

#### Script Functions

- 150+ new functions and 10+ event handlers, including WorldToScreen, SetVelEx, GetTimePlayed and more.
- Complete list of added functions with documentation and examples can be found on GECK Wiki.


#### New features

- **Runtime Editor IDs:** GECK Editor IDs can now be used in game console (e.g. "player.additem weap10mmpistol") and in scripts as dynamic string variables using GetEditorID and EditorIDToFormID functions. Additionally, Editor IDs are now displayed when you select a reference without a name in game console.
- **Custom Map Marker Icons:** SetCustomMapMarkerIcon function lets you override hardcoded map marker icons with your own.
- **Level Up Menu Toggle:** ToggleLevelUpMenu and IsLevelUpMenuEnabled functions let you disable or delay level up menu display.
- **Event Framework:** JGCreateEvent and JGFreeEvent functions are exported to allow other plugin authors to take advantage of JohnnyGuitar's event system. See headers in events folder in the source code for example usage.



#### Bugs fixed

These fixes do not conflict with identical fixes in other NVSE plugins. Optional fixes enabled in JohnnyGuitar.ini are marked with *.

 - **Rapid Reload fix:** Reload and holster speed are now correctly recalculated after loading a save.
 - **Disintegrations Stat fix:** "Disintegrations" stat no longer increases upon entering a cell containing an ash pile.
 - **Water Consumed fix:** "Water Consumed" stat now increments properly.
 - **Companion Dialogue fix:** Companions are no longer rendered mute after trading with them through dialogue.
 - **VATS spread fix:** fNPCMaxGunWobbleAngle setting no longer affects player spread calculations in VATS.
 - **Animated Dialogue fix:** Dialogue topics with both animation and sound specified now correctly play animation.
 - **NPC Challenge fix**: NPCs no longer increment player challenges with "Use Item" or "Use Item from a List" type by equipping items.
 - **Inventory Ammo Display fix:** While hovering over a weapon that you don't have a default ammo for, item card will use a different ammo type from the inventory for ammo count, damage and DPS calculation.
 - **3rd Person Camera fix:** After using Vanity camera, 3rd Person camera position correctly resets.
 - **Gun Spread Calculation fix: fWeapSkillReqPenalty setting is now used correctly.
 - ***Fake fleeing fix:** NPCs will no longer flee from the player when [CAUTION] state is active but there are no enemies around.
 - ***Item Stack Count fix:** Dropping a stack of more than 32000 items from inventory will no longer cause the item count to overflow into negatives, multiple item stacks will be dropped instead.
 - **Weapon Biped Model Update fix**:
    - Weapons that have backpacks and weapon mods will no longer create duplicates of the backpack when unequipped/equipped.
    - Hotkeyed weapons with weapon mods will no longer force play the reequip animation.
    - Loading a save with a weapon with weapon mods will no longer cause the projectile node to be misplaced.
    - Reequipping any apparel while having a weapon with mods equipped will no longer cause the weapon to reequip too.
    - Weapons with backpacks will no longer have the backpack still appear on the player or actor after using RemoveAllItems/RemoveAllTypedItems.
 - **Incidental Media Set fix**: Incidental-type media sets now work correctly in all DLCs and mods. They were working only in FalloutNV.esm and DeadMoney.esm before.
 - ***Close Range Shooting Angle fix**: NPCs now properly turn towards the player before shooting while in close range.

#### Requirements:
- [xNVSE 6.1.6 or newer](https://github.com/xNVSE/NVSE/releases/latest)﻿
 
#### [Download](https://github.com/carxt/JohnnyGuitarNVSE/releases/latest)
 
Created and maintained by lStewieAl, c6, and carxt, with contributions and help from jazzisparis, Nukem and korri123.
