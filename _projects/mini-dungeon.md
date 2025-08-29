---
title: <span style="color:Chartreuse">**Mini Dungeon**
excerpt: <span style="color:azure">*A classic text-based RPG console game featuring dungeon exploration, combat mechanics, and progression based on items*
header:
    teaser: /assets/images/projects/mini-dungeon/welcome-to-mini-dungeon.png
    overlay_image: /assets/images/projects/mini-dungeon/mini-dungeon-project-banner.jpg
    overlay_filter: linear-gradient( rgba(5, 5, 5, 0.5), rgba(0, 255, 55, 0.5))
    caption: "Photo credit: [**Tobias_ET**](https://pixabay.com/illustrations/matrix-computer-hacker-code-2354492)"
    actions:
        - label: "View on GitHub"
          url: "https://github.com/L-Pace/MiniDungeon/tree/master"
        - label: "Download"
          url: "https://misdur.itch.io/mini-dungeon"
          
tags:
    - C#
    - Game Development
    - Text-based RPG
    - Console Application
    - Solo Project
    - Object-Oriented Programming

date: 2024-08-28
---

# Project Overview
![image-center](/assets/images/projects/mini-dungeon/welcome-to-mini-dungeon.png){: .align-center}

*Mini Dungeon* is a text-based RPG built as a C# console application, inspired by traditional dungeon crawler games. This project demonstrates my programming fundamentals, object-oriented design principles, and ability to create engaging gameplay mechanics through code alone.  

**Development Time**: <span style="color:Chartreuse">2 months</span> \
**Team Size**: <span style="color:Chartreuse">Solo project</span> \
**Role**: <span style="color:Chartreuse">Programmer & Game Desisgner</span> \
**Platform**: <span style="color:Chartreuse">Console Application (Windows)</span> 
 
# Key Features
## 📜 Handcrafter Dungeon Map and City Map
The map is based on my idea to integrate my university life in Cambridge City in a small fantasy RPG including my teachers as NPCs, mini-Bosses and final Boss. I created one single map that included several interconnected location:

* Home
* Compass House (Town)
  * The White Horse Tavern
  * The Nerd Shrine (Shop)
  * Ian, The Alchemist House
* The Red Forest
  * The Cabin in The Woods
  * The Red Lake
* The Mini Dungeon
  * Entrance
  * Three Dungeon Rooms
  * Throne Room

![image-left](/assets/images/projects/mini-dungeon/mini-dungeon-screenshots/mini-dungeon-map-prototype-1.jpg "I wanted to make a secret entrance to the dungeon but at the end I dind not included it."){: .align-left} ***Figure 1**: Mini Dungeon Map prototype*

![image-right](/assets/images/projects/mini-dungeon/mini-dungeon-screenshots/mini-dungeon-map-prototype-2.jpg){: .align-right} ***Figure 2**: Mini Dungeon Map prototype with the final dungeon map*

## ⚔️ Turn-based Combat System
The combat system is the ancestor of every primordial RPGs: it is a strategic turn-based mechanics that requires a small tactical thinking.
The damage calculation is a mathematical combat system with attack, defence, and health system.

```cs
private static void PlayerTurn()
{
  int damageToMonster;
  int monsterDefense;
  int effectiveDamageToMonster;

  monsterDefense = RandomNumberGenerator.NumberBetween(_currentMonster.MinimumProtection,
                                                      _currentMonster.MaximumProtection);
  if (_character.newPlayer.MinimumDamage != 0 && _character.newPlayer.MaximumDamage != 0)
  {
    damageToMonster = RandomNumberGenerator.NumberBetween(_character.newPlayer.MinimumDamage,
                                                          _character.newPlayer.MaximumDamage);
    effectiveDamageToMonster = PlayerTurnReport(damageToMonster, monsterDefense);
  }
  else
  {
    damageToMonster = RandomNumberGenerator.NumberBetween(_character.newPlayer.ClassMinimumDamage,
                                                          _character.newPlayer.ClassMaximumDamage);
    effectiveDamageToMonster = PlayerTurnReport(damageToMonster, monsterDefense);
  }
}                    
```

```cs
private static int CalcEffectiveDamageToMonster(int damageToMonster, int monsterDefense)
{
  int effectiveDamageToMonster = damageToMonster - monsterDefense;
  if (effectiveDamageToMonster <= 0)
  {
    effectiveDamageToMonster = 0;
  }
  else
  {
    _currentMonster.CurrentHitPoints -= effectiveDamageToMonster;
  }
  return effectiveDamageToMonster;
}
```
```cs
/// <summary>
/// Report of the player turn
/// </summary>
/// <param name="damageToMonster">Player attack power</param>
/// <param name="monsterDefense">Monster defense power</param>
/// <returns></returns>
private static int PlayerTurnReport(int damageToMonster, int monsterDefense)
{
  int effectiveDamageToMonster;
  Console.Clear();
  Console.WriteLine(fightText);
  Console.WriteLine();
  Console.WriteLine("** Your turn ***");
  Console.WriteLine();
  Console.WriteLine("You attacking with " + damageToMonster + " hit point/s.");
  Console.WriteLine(_currentMonster.Name + " is defending with " + monsterDefense + " armor points.");

  effectiveDamageToMonster = CalcEffectiveDamageToMonster(damageToMonster, monsterDefense);

  Console.WriteLine("You hit " + _currentMonster.Name + " for " + effectiveDamageToMonster.ToString() + " point/s.");
  Console.WriteLine("The " + _currentMonster.Name + " has " + _currentMonster.CurrentHitPoints + " HP left.");
  Console.Write("[Enter] to continue...");
  Console.ReadKey();
  Console.WriteLine();
  return effectiveDamageToMonster;
}
```


## RPG Mechanics
## Text-based Interface

# Technical Implementation
## Core Technologies

# Key Classes & Systems
## Game Manager
## Player Character System
## World Map & Dungeon Map

# Technical Challanges & Solutions
## Challange 1
## Challange 2
## Challange 3

# Game Flow & Architecture
## Command Processing System
## Data Structure Design
## Game States

# Code Architecture Principles
## Design Patterns Applied
## Object-Oriented Features

# Screenshots & Console Outputs

# Learning Outcomes
## Programming skills developed
## Game Development Insights

# What I Learned

# Technical Specifications

# Future Improvements

# Links