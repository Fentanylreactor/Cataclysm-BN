# A Beginners guide to contributing 

If you have, at any point, thought that something was missing from the game, or wanted to help the project, look no further! 

The scope of this document is to teach you how to contribute to **Bright Nights** from ground up.

First, This is a list of things you can change/make with zero/barely any coding experience :

* Monsters (Mutated flying clams) and Zombies (Electric dissoluted devourer, flying shoggoths, etc.) 
* Weapons (Superalloy katana) and Armor (Superalloy power armor) 
* Terrain (Marble tiles, new walls and doors, etc.) and Furniture (New lamps, indoor plants, etc.) 
* Vehicle parts (Superalloy roller drum, water powered engine, etc) and Vehicles (Tanks, AT, etc.) 
* New locations (like houses or military bases)
* Spells (Summon anvil, cast internal combustion) and Enchants (When it's day i get +5 STR) 
* Most Mutations, Bionics and Effects 

The tools required :

**A github account**
**A text editor** (Notepad suffices but Notepad++, Vscode and many others can make your life easier and are free, notepad++ in particular is easy to set up)

Once you have those you are ready to start contributing!

But first, coding and contributing isn't black magic, this is what you will be working with:

```
{
  "id": "mon_zombie", 
  "type": "MONSTER",
  "name": {
    "str": "zombie"
  },
  "description": "A human body, swaying as it moves, an unstoppable rage visible in its oily black eyes.",
  "default_faction": "zombie",
  "bodytype": "human",
  "categories": [
    "CLASSIC"
  ],
  "species": [
    "ZOMBIE",
    "HUMAN"
  ],
  "volume": "62500 ml",
  "weight": "81500 g",
  "hp": 80,
  "speed": 70,
  "material": [
    "flesh"
  ],
  "symbol": "Z",
  "color": "light_green",
  "aggression": 100,
  "morale": 100,
  "melee_skill": 4,
  "melee_dice": 3,
  "melee_dice_sides": 3,
  "melee_cut": 0,
  "vision_night": 3,
  "harvest": "zombie",
  "special_attacks": [
    {
      "type": "bite",
      "cooldown": 5
    },
    [
      "GRAB",
      7
    ],
    [
      "scratch",
      20
    ]
  ],
  "death_drops": "default_zombie_death_drops",
  "death_function": [
    "NORMAL"
  ],
  "fungalize_into": "mon_zombie_fungus",
  "burn_into": "mon_zombie_scorched",
  "upgrades": {
    "half_life": 14,
    "into_group": "GROUP_ZOMBIE_UPGRADE"
  },
  "flags": [
    "SEES",
    "HEARS",
    "SMELLS",
    "STUMBLES",
    "WARM",
    "BASHES",
    "GROUP_BASH",
    "POISON",
    "BLEED",
    "NO_BREATHE",
    "REVIVES",
    "PUSH_MON"
  ]
}
```
This is ALL the JSON that goes into a basic zombie. 

If you want it to be faster, increase it's speed. Survive more hits? Increase its HP (hit points). 

With that out of the way, let's begin! 

- - -

# Getting started:

1. Go to the main page of [the game](<https://github.com/cataclysmbn/Cataclysm-BN?tab=readme-ov-file>)

2. Fork the game (not a typo) :

Placeholder text until i get image here

Placeholder text until get second image here

> Explanation: You made your own copy of the game on your github account. Your changes will first be applied here, then you request them to be added to the main game. (explained later) 

> it is my personal recommendation to keep both your offline game and your github repo as often updated as possible. New features get added often and you might miss something that could make your life easier.



