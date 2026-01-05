If you have, at any point, thought that something was missing from the game, or wanted to help the project, look no further! 

The scope of this document is to teach you how to contribute to Bright Nights from ground up.

First, This is a list of things you can change/make with zero/barely any coding experience :

> Monsters and Zombies 
> Weapons and Armor 
> Terrain and Furniture
> Vehicle parts and Vehicles
> Mapgen (like houses or military bases)
> Spells and Enchants 
> Most Mutations, Bionics and Effects 

The tools required :

A github account
A text editor (Notepad suffices but notepad++, vscode and many others can make your life easier and are free, notepad++ in particular is easy to set up)

Once you have those you are ready to start contributing!

But first, making content really isn't the black magic people assume it is:

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
This is ALL the json that goes into a basic zombie. Surprisingly simple, right?

With that out of the way, let's begin! 

- - -

First, go to the main page of [the game](<https://github.com/cataclysmbn/Cataclysm-BN?tab=readme-ov-file>)

Second, fork the game (not a typo) :

Placeholder text until i get image here

Placeholder text until get second image here

You now have copied the games files onto your own github account, every change you implement will first show up here, and them you simply request (explained a bit later) for them to be added to the main game. 



