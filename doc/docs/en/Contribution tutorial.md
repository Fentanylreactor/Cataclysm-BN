# A Beginners guide to contributing 

If you have, at any point, thought that something was missing from the game, or wanted to help the project, look no further! 

The scope of this document is to teach you how to contribute to Bright Nights from ground up.

First, This is a list of things you can change/make with zero/barely any coding experience :

* Monsters (Flying cats and dogs, laser triffid) and Zombies (Electric dissoluted devourer, flying shoggoths, etc.) 
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

If you want it to be faster, increase it's speed. Survive more hits? Increase its HP. 
Make it unable to BASH down walls and windows? Remove BASHES flag. 
Make it blind? Remove SEES flag. 

With that out of the way, let's begin! 

- - -

# Getting started:

1. Go to the main page of [the game](<https://github.com/cataclysmbn/Cataclysm-BN?tab=readme-ov-file>)

2. Fork the game (not a typo) :

Placeholder text until i get image here

Placeholder text until get second image here

> Explanation: You made your own copy of the game on your github account. Your changes will first be applied here, then you request them to be added to the main game. (explained later) 

> it is my personal recommendation to keep both your offline game and your github repo as often updated as possible. New features get added often and you might miss something that could make your life easier.

---

# Navigating

All of the data in this game is stored under `data/json`. 

Each folder here houses it's appropriate json files, like `recipes` housing recipes, `items` housing items, `vehicles` having vehicle blueprints, etc. 

# Copy-Paste

**It is far easier to copy something that exists and modify it than to write json from scratch**

Find the json code of something that's similar to what you want. Then edit it. To cover everything here would take quite a bit of time, I would recommend that you look through [the modding guide](<https://www.leagueoflegends.com/ro-ro/download>) because the json for modding and json for contributions are the same.

# Editing

How to json:

1. Every ID, without exceptions, must be unique. 

2. Brackets. If there is an opening one, there is a closing one.

3. Every line ends in a comma, except the last `}` in the file and last line in object (look at the zombie example).

Number changes are easy.
**Str**ings (the text displayed in game, aka `"str" : "zombie",`) are also easy. 

Flags, if they are on a similar thing, will almost always work. You can make a zombie dig for example, but you can't give it the flag to leak radiation if damaged (from thermoblade). You can do that in other ways. 

The simplest way to do it is to copy paste the entire block from the it's opening `{` to its closing `}`, then pasting it in between two other entries. 

> Some editors like vscode and notepad++ show you which bracket corresponds to which.

After you do your changes, check if there's an entry under what you pasted. If yes, make sure theres a comma behind the `}`. 

# How to edit

There's two ways you can do the editing.

Find the files in your game and make the changes there, and launch the game. If you can load into a world, spawn the object and it behaves normally, you did it!

If it doesn't, read the red debug message, it will always tell you what you did wrong, and what line you mightve missed a comma or similar.

> Tip : Don't close the folder you're editing in. Saves time if there's issues.

The other way of doing it.

Applying your changes to your repo by editing code there. Then downloading the file and replacing the exact same file in your installation directory.

The other other way is opening github codespaces. Not for everyone.

- - -

# The pull request ( aka add this to the main game request)

Your changes work? Great, now open YOUR fork, and find the folder where the file goes inside your current offline install.

The file names inside the folders should match.

Upload your file and overwrite it.

Then you start a pull request to the main repository:

Image here
Image here

You look through the description of the pull request text, and filling out the form.

Why should it be added? It's cool. It's good. It fits. Etc.

Then you type x in a few boxes.

Make sure the "Allow repository owners to make changes" box is ticked, otherwise it can be held up for a long time over trivial changes.

Press the green pull request button.

Done!

You have created a pull request for your content/change to be added to the main game. 
