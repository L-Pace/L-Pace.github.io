---
title: "**Cosmic Control Enterprises**"
excerpt: "A puzzle game inspired from *'Please, don't touch anything!'* and the book series 'The Expanse'"
header:
    teaser: /assets/images/projects/cosmic-control-enterprises/cce-thumb.png
    overlay_image: /assets/images/projects/cosmic-control-enterprises/cce-banner.jpg
    overlay_filter: linear-gradient( rgba(0, 17, 255, 0.2), rgba(162, 0, 255, 0.5))
    caption: "Photo credit: [**geralt**](https://pixabay.com/illustrations/universe-heaven-stars-space-cosmos-1566159)"
    actions:
        - label: "View on GitHub"
          url: "https://github.com/L-Pace/cosmic-control-enterprises"
        - label: "Download"
          url: "https://misdur.itch.io/cosmic-control-enterprises"

tags:
    - Unity
    - C#
    - Game Development
    - Puzzle Game
    - Indie Games

date: 2024-09-08

gallery:
    - url: /assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-screenshot-1.png
      image_path: /assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-screenshot-1.png
      alt: "Rocinante"
      title: "The Spaceship Rocinante"

    - url: /assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-screenshot-2.png
      image_path: /assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-screenshot-2.png
      alt: "Interior"
      title: "Interior detail 1"

    - url: /assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-screenshot-3.png
      image_path: /assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-screenshot-3.png
      alt: "Interior"
      title: "Interior detail 2"

    - url: /assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-screenshot-4.png
      image_path: /assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-screenshot-4.png
      alt: "Interior"
      title: "Interior detail 3"

    - url: /assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-screenshot-6.png
      image_path: /assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-screenshot-6.png
      alt: "Interior"
      title: "Interior detail 4"
    
    - url: /assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-screenshot-5.png
      image_path: /assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-screenshot-5.png
      alt: "Loading Screen"
      title: "Loading Screen"
---
# Project Overview
![image-center](/assets/images/projects/cosmic-control-enterprises/cce-thumb.png){: .align-center}
*Cosmic Control Enterprises* is a puzzle game set up on *The Expanse* (**James S. A. Corey, 2011**), one of the most well-known science fiction book series adapted into a successful TV show. I attempted to give the player the impression that they were in control of a crucial mission, starting the game inside the room I constructed using the assets pack provided by the university: save the Rocinante’s crew first and preserve humanity's one remaining chance to explore alien worlds and settle habitable planets in the Milky Way and beyond. 
It is obvious that the game *Please, don't touch anything!* (**Four Quarters team, 2015**) was the inspiration for this one. 

**Development Time**: <span style="color:Chartreuse">3 weeks</span> \
**Team Size**: <span style="color:Chartreuse">Solo project</span> \
**Role**: <span style="color:Chartreuse">Programmer & Game Desisgner</span> \
**Platform**: <span style="color:Chartreuse">Unity</span> 

# Screenshots
{% include gallery caption="Some screenshots of the game" %}

# Key Features
## 🌌 Sci-fi background
For this project I decided to use the [Synty Polygon - Sci-Fi Space Pack](https://syntystore.com/en-gb/products/polygon-sci-fi-space-pack?_pos=2&_sid=12c8ce5a0&_ss=r) perfect for the set up of this game (see **Figure 1**).

![image-center](/assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-synty-assets-pack.png "Synty Sci-Fi Space Pack in action"){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 1:</b></i> <i>Synty Sci-Fi Space Pack</i></p>

## ⚙️ Interacting with The Puzzles
The puzzle in game are available step by step after completing a series of action by the player. The player can just move the camera and interact with the main console (see **Figure 2**).

![image-center](/assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-main-console.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 2:</b></i> <i>Main Console</i></p>

## ⚡ Hint
A hint to opening the safe has been hidden in one of the computer screens (see **Figure 3 and 4**). I decided to use the number 6765 from the Fibonacci sequence to help the player address an easy mathematics problem.

![image-center](/assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-hint2.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 3:</b></i> <i>Error Console</i></p><br>

![image-center](/assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-hint2-detail.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 4:</b></i> <i>Hint Detail</i></p>


## 🧑‍🚀 Win & Lose Conditions
### 🚀 Win Condition
To access the “Win screen” (see **Figure 5**), players must complete a series of puzzles in the game within 5 minutes countdown(see **Figure 6**). In the first, the player must learn how to press specific buttons to activate the various consoles.

![image-center](/assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-screenshot-win.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 5:</b></i> <i>Win Screen</i></p><br>

![image-center](/assets/images/projects/cosmic-control-enterprises/cce-screenshots/cee-countdown.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 6:</b></i> <i>Countdown</i></p>

### 💥 Lose Condition
If the player is not able to finish the puzzle within 5 minutes, they will get a Lose Screen (see **Figure 7**).

![image-center](/assets/images/projects/cosmic-control-enterprises/cce-screenshots/cce-screenshot-lose.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 7:</b></i> <i>Lose Screen</i></p>

# Technical Implementation
## ✨ Interaction System

## 🧾 Menus
### 🖥️ Main Menu
### 🎮 Text Tutorial
### 🔧 Settings Menu

## ⏱️ The Timer

## 🧠 Main Puzzles Overview 
### 🧩 Keypad Puzzle
### 🧩 Pipe Puzzle


# Critical Evaluation

# External Assets

# References
Corey, J. S. A. (2011) *The Expanse*. United States: Orbit Books.

Four Quarters team (2015) *Please, don’t touch anything!* Available at: [Please, don't touch anything](https://fourquarters.itch.io/pdta-ld) (Accessed: 22 August 2024)

 