---
title: "**Audio Programming Prototype**"
excerpt: '*An artifact that shows the power of FMOD middleware with Unreal Engine*'
header:
    teaser: /assets/images/projects/audio-programming/ap-thumbnail.png
    overlay_image: /assets/images/projects/audio-programming/ap-banner.png
    overlay_filter: linear-gradient( rgba(5, 5, 5, 0.7), rgba(39, 37, 161, 0.7))
    actions:
        - label: "Watch on YouTube"
          url: "https://youtu.be/GKmEGeXDGeE"
        - label: "Download the Documentation"
          url: "https://misdur.itch.io/audio-programming-prototype-documentation"          
tags:
    - Unreal Engine 5
    - Game Development
    - Solo Project
    - Blueprints
    - Audio Programming
    - FMOD Studio
    - Prototype
    - Sound Design

date: 2023-04-25

gallery:
    - url: /assets/images/projects/audio-programming/Screenshots/Picture1.png
      image_path: /assets/images/projects/audio-programming/Screenshots/Picture1.png
      alt: "Artefact with 3 different kinds of surfaces and 2 ambience cues"
      title: "Artefact with 3 different kinds of surfaces and 2 ambience cues"

    - url: /assets/images/projects/audio-programming/Screenshots/screenshot-2.png
      image_path: /assets/images/projects/audio-programming/Screenshots/screenshot-2.png
      alt: "Fader"
      title: "Fader"

    - url: /assets/images/projects/audio-programming/Screenshots/screenshot-3.png
      image_path: /assets/images/projects/audio-programming/Screenshots/screenshot-3.png
      alt: "Big Room Int"
      title: "Big Room Int"

    - url: /assets/images/projects/audio-programming/Screenshots/screenshot-1.png
      image_path: /assets/images/projects/audio-programming/Screenshots/screenshot-1.png
      alt: "Logic Track - Grass"
      title: "Logic Track - Grass"

    - url: /assets/images/projects/audio-programming/Screenshots/figure-1.png
      image_path: /assets/images/projects/audio-programming/Screenshots/figure-1.png
      alt: "Footsteps Event"
      title: "Footsteps Event"
    
    - url: /assets/images/projects/audio-programming/Screenshots/figure-2.png
      image_path: /assets/images/projects/audio-programming/Screenshots/figure-2.png
      alt: "Player/Footsteps attached to PlayerSFX Bank"
      title: "Player/Footsteps attached to PlayerSFX Bank"
    
    - url: /assets/images/projects/audio-programming/Screenshots/figure-3.png
      image_path: /assets/images/projects/audio-programming/Screenshots/figure-3.png
      alt: "Timeline with all the footsteps sound"
      title: "Timeline with all the footsteps sound"

    - url: /assets/images/projects/audio-programming/Screenshots/figure-4.png
      image_path: /assets/images/projects/audio-programming/Screenshots/figure-4.png
      alt: "Random Post-process effect on Volume and Pitch"
      title: "Random Post-process effect on Volume and Pitch"

    - url: /assets/images/projects/audio-programming/Screenshots/figure-5.png
      image_path: /assets/images/projects/audio-programming/Screenshots/figure-5.png
      alt: "SurfaceType"
      title: "SurfaceType"

    - url: /assets/images/projects/audio-programming/Screenshots/figure-6.png
      image_path: /assets/images/projects/audio-programming/Screenshots/figure-6.png
      alt: "Grass Automation Volume and 3-EQ"
      title: "Grass Automation Volume and 3-EQ"

    - url: /assets/images/projects/audio-programming/Screenshots/figure-12.png
      image_path: /assets/images/projects/audio-programming/Screenshots/figure-12.png
      alt: "Physical Surface"
      title: "Physical Surface"

    - url: /assets/images/projects/audio-programming/Screenshots/figure-15.png
      image_path: /assets/images/projects/audio-programming/Screenshots/figure-15.png
      alt: "Grass Surface"
      title: "Grass Surface"

    - url: /assets/images/projects/audio-programming/Screenshots/figure-17.png
      image_path: /assets/images/projects/audio-programming/Screenshots/figure-17.png
      alt: "The actual bird chirping from FMOD found in the Unreal Engine Folder"
      title: "The actual bird chirping from FMOD found in the Unreal Engine Folder"
    
    - url: /assets/images/projects/audio-programming/Screenshots/figure-18.png
      image_path: /assets/images/projects/audio-programming/Screenshots/figure-18.png
      alt: "Snapshot Reverb - Attack and Release"
      title: "Snapshot Reverb - Attack and Release"

published: true
---

# Project Overview

{% include video id="GKmEGeXDGeE" provider="youtube" %}

This audio programming project demonstrates the implementation of dynamic, immersive audio systems using FMOD Studio integrated with Unreal Engine 5.2. Inspired by AAA titles like *Ghost of Tsushima* and *Red Dead Redemption 2*, the project focuses on creating responsive audio that enhances player immersion through surface-based footsteps, spatial ambience, and environmental reverb.
The artefact showcases a third-person character with dynamic footstep sounds that change based on three different surface types (grass, wood, concrete), complemented by adaptive ambient soundscapes including spatially-aware bird chirping and interior room reverb with atmospheric lighting hum.

**Development Time**: <span style="color:Chartreuse">1 months</span> \
**Team Size**: <span style="color:Chartreuse">Solo project</span> \
**Role**: <span style="color:Chartreuse">Audio Programmer & Sound Designer</span> \
**Platform**: <span style="color:Chartreuse">PC</span>

# Screenshots
{% include gallery caption="Some screenshots FMOD and the prototype" %}

# Technical Focus

This project explores the complexities of audio programming in interactive environments, examining:

- **Middleware Integration**: Manual FMOD Studio integration with Unreal Engine 5.2
- **Dynamic Audio Systems**: Surface-detection and parameter-driven sound switching
- **Spatial Audio**: 3D positioned ambient cues with distance attenuation
- **Adaptive Soundscapes**: Context-aware reverb and environmental audio transitions
- **Animation Synchronization**: Precise footstep timing using animation notifications

# Key Features
## 🎵 Dynamic Footstep System

- **Multi-Surface Detection**: Three distinct surface types with unique audio characteristics

  - **Grass**: Soft, muffled steps with natural vegetation sounds
  - **Wood**: Crisp, hollow footsteps with slight resonance
  - **Concrete**: Solid, clear impact sounds for paved surfaces


- **Procedural Variation**: Randomized pitch and volume for each footstep to prevent repetition
- **Animation Sync**: Perfectly timed footstep sounds using Unreal Engine animation notifies
- **3-Band EQ Processing**: Dynamic frequency adjustments for different materials

# 🌳 Adaptive Ambient Soundscape
- **Exterior Ambience**: Spatially-positioned bird chirping with distance-based attenuation
- **Scattered Audio Placement**: Multiple bird sounds distributed naturally across the environment
- **Interior/Exterior Blending**: External sounds audibly muffled when entering enclosed spaces
- **Proximity-Based Volume**: Dynamic sound levels as player approaches or leaves ambient sources

# 🏛️ Environmental Reverb System

- **Large Room Simulation**: Natural reverberation effect for enclosed spaces
- **Snapshot-Based Transitions**: Smooth reverb activation when entering interior spaces
- **Contextual Footsteps**: Modified footstep sounds reflecting room acoustics
- **Interior Ambience**: Atmospheric lightbulb buzz/hum adding to environmental presence
- **Wall Occlusion**: External sounds properly muffled through walls

# Technical Implementation
## FMOD Studio Architecture
### Footsteps Event System
The footstep system uses a parameter-driven approach with automatic surface detection:

```bash
Event: Player/Footsteps
├── Timeline (4 Audio Tracks)
│   ├── Grass (3 variations)
│   ├── Wood (3 variations)
│   ├── Concrete (3 variations)
│   └── Default (3 variations)
├── Parameter: SurfaceType (0-3)
└── Effects Chain
    ├── Random (Pitch: ±5%, Volume: ±3dB)
    ├── 3-Band EQ (per-surface)
    └── Volume Automation
```

### Parameter Automation Logic

- <span style="color:Red"><b>SurfaceType = 0</b></span>: Grass sounds at 0dB, others muted 
- <span style="color:Red"><b>SurfaceType = 1</b></span>: Wood sounds at 0dB, others muted
- <span style="color:Red"><b>SurfaceType = 2</b></span>: Concrete sounds at 0dB, others muted
- <span style="color:Red"><b>SurfaceType = 3</b></span>: Default sounds at 0dB, others muted

Each surface track includes three variations to prevent audio repetition, with randomized pitch (±5%) and volume (±3dB) for natural variation.

## Ambient Audio Configuration
### Birds Chirping (Exterior)

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-16.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 1: </b></i><i>Birds Chirping Ambience Cue</i></p>

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-8.png){: style="width:800x" .align-center}
<p style="text-align:center;"><i><b>Figure 2: </b></i> <i>Settings for the Birds Chirping</i></p>

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-7.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 3: </b></i> <i>Birds Chirping sounds</i></p>

```bash
Event: Ambience/BirdsChirping
├── Scattered Instrument (5 bird variations)
├── Spawn Interval: 2-5 seconds
├── Scatter Distance: 15m radius
└── Effects
    ├── Random Pitch (±10%)
    └── Random Volume (±5dB)
```

### Interior Ambience

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-9.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 4: </b></i><i>Lightbulb buzz/hum track</i></p>

```bash
Event: Ambience/LightbulbHum
├── Looping Audio Track
├── Mixer Group: AmbienceInt
└── Snapshot-Controlled Reverb
```

## Mixer Architecture & Snapshots
The FMOD mixer uses grouped routing for precise control:

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-10.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 5: </b></i><i>Mixer</i></p>


```bash
Master Bus
├── AmbienceExt (External Sounds)
│   └── Birds Chirping
├── AmbienceInt (Internal Sounds)
│   └── Lightbulb Hum
├── PlayerSFX (Character Sounds)
│   └── Footsteps
└── Return: BigRoom (Reverb)
    ├── Attack: 0.5s
    └── Release: 1.0s
```

### Snapshot: BigRoom Interior

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-11.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 6: </b></i><i>Snapshot of AmbienceInt</i></p>

- Activates reverb return bus
- Attenuates external ambience by -6dB
- Applies low-pass filter to external sounds (simulating wall occlusion)
- Smooth 500ms transition in/out

## Unreal Engine 5 Integration
### Physical Surface Setup
```cpp
// Project Settings > Physics > Physical Surfaces
PM_Grass    (SurfaceType1) = 0
PM_Wood     (SurfaceType2) = 1  
PM_Concrete (SurfaceType3) = 2
PM_Default  (Default)      = 3
```

### Animation Blueprint Logic
Character footsteps triggered via animation notifies:

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-14.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 7: </b></i><i>Footsteps notifies</i></p>

```bash
Animation: ThirdPersonRun
├── Notify: LeftFoot (Frame 15)
│   └── Play FMOD Event 2D (Player/Footsteps)
│       └── Set Parameter: SurfaceType (from trace hit)
└── Notify: RightFoot (Frame 45)
    └── Play FMOD Event 2D (Player/Footsteps)
        └── Set Parameter: SurfaceType (from trace hit)
```

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-13.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 8: </b></i><i>Character Animation Blueprint</i></p>

### Surface Detection System
1. Line trace from character foot to ground
2. Query physical material of hit surface
3. Convert material to SurfaceType parameter value
4. Pass parameter to FMOD event before playback

### Spatial Audio Placement
Ambient cues placed as 3D FMOD Audio components:

- **Birds Chirping**: Positioned near grass area with 30m max distance
- **Lightbulb Hum**: Inside big room, 15m max distance
- **Snapshot Trigger**: Box collision volume activating BigRoom snapshot

# Technical Challenges & Solutions
## Challenge 1
### Manual FMOD Integration with UE5.2
**Problem**: No official marketplace plugin available for Unreal Engine 5.2
**Solution**: Manually integrated FMOD by:

1. Downloaded FMOD Studio and Unreal Engine integration files
2. Created Plugins folder in project directory
3. Extracted FMOD plugin files into Plugins/FMODStudio
4. Regenerated Visual Studio project files
5. Compiled plugin from source
6. Created new FMOD Studio project and linked to Unreal project via settings
7. Built initial bank structure and validated integration

**Learning**: Understanding plugin architecture and manual integration process deepened knowledge of Unreal Engine's plugin system

## Challenge 2 
### Animation-Footstep Synchronization
**Problem**: Footstep sounds playing inconsistently or out of sync with character animations

**Solution**:

1. Created dedicated notify track in animation sequence
2. Placed notifies precisely at foot-contact frames
3. Added separate "L" and "R" notifies for complete animation montage
4. Tested sync across different animation speeds
5. Fine-tuned notify positions through iterative playtesting

**Result**: Perfect synchronization between visual footstep and audio playback at all animation speeds

## Challenge 3
### Interior Reverb Bleed
**Problem**: Reverb effect persisting for 2-3 seconds after leaving the big room

**Solution**:

- Adjusted snapshot Attack time to 500ms (entering room)
- Set Release time to 1000ms (leaving room)
- Optimized reverb tail length in effect chain
- Reduced pre-delay to minimize latency

**Result**: Reverb now dissipates within 1 second of leaving interior space, providing responsive environmental transition

## Challenge 3
### External Audio Occlusion
**Problem**: Bird sounds too prominent inside the big room, breaking immersion

**Solution**:

- Routed external ambience through dedicated mixer group
- Created snapshot that attenuates AmbienceExt by -6dB
- Applied low-pass filter (cutoff: 2kHz) when snapshot active
- Maintained spatial 3D positioning for realistic directionality

**Result**: External sounds appropriately muffled when inside, while maintaining spatial awareness of their location

# Audio Design Philosophy
## Inspiration from AAA Games

***Ghost of Tsushima*** - Primary inspiration for footstep variety and environmental ambience placement. The seamless integration of natural sounds with character movement heavily influenced this project's approach.

***Red Dead Redemption 2*** - Studied for comprehensive ambient soundscape design and how environmental audio responds to player location.

***Subnautica*** - Referenced for underwater audio manipulation techniques, adapted here for interior/exterior transitions.

***No Man's Sky*** - Examined for dynamic surface-based audio and cockpit ambience design principles.

## Design Principles Applied
**Seamless Transitions**: Surface changes detected instantly with no audio pops or gaps

**Natural Variation**: Randomization prevents audio fatigue while maintaining authenticity

**Spatial Awareness**: 3D audio positioning helps players understand their environment

**Contextual Adaptation**: Audio responds appropriately to player's location and actions

**Performance Optimization**: Efficient event streaming and memory management for real-time audio

# System Architecture Benefits
## For Designers
- **No-Code Audio Editing**: All audio parameters adjustable in FMOD Studio
- **Visual Event Creation**: Timeline-based interface for complex audio behaviors
- **Live Tuning**: Real-time parameter adjustments while game is running
- **Clear Organization**: Logical event/bank structure for easy navigation

## For Programmers

- **Clean Integration**: Well-defined interface between FMOD and Unreal
- **Parameter-Driven**: Single event handles multiple variations via parameters
- **Memory Efficient**: Streaming system loads only necessary audio
- **Scalable Architecture**: Easy to add new surfaces or ambient cues

## For Players

- **Enhanced Immersion**: Responsive audio that reflects their actions
- **Environmental Awareness**: Audio cues provide gameplay information
- **Natural Soundscape**: Varied, realistic audio prevents monotony
- **Smooth Experience**: No jarring transitions or audio glitches

# Learning Outcomes
## Technical Skills Developed
**Audio Middleware Mastery**: Deep understanding of FMOD Studio's event system, mixer architecture, and parameter automation

**Integration Expertise**: Manual plugin integration, understanding build systems and engine architecture

**Spatial Audio**: 3D positioning, distance attenuation, occlusion simulation, and reverb zones

**Performance Optimization**: Audio streaming, memory management, and event instantiation best practices

**Signal Processing**: Applied EQ, compression, reverb, and randomization for realistic audio

## Game Development Insights
**Audio Programming Workflow**: Understanding the complete pipeline from sound design to in-game implementation

**Cross-Discipline Communication**: Learning to think from both programmer and sound designer perspectives

**Iteration Importance**: Multiple testing cycles crucial for achieving natural-feeling audio

**Documentation Value**: Clear technical documentation essential for complex audio systems

**Scope Management**: Balancing ambition with timeline constraints and technical limitations

# Future Enhancements
If expanding this project, I would implement:

## Dynamic Music System

- Adaptive music that responds to player actions
- Vertical layering based on intensity/danger
- Smooth transitions between exploration and combat themes

## Advanced Occlusion

- Real-time raycast-based audio occlusion
- Material-based filtering (wood walls vs concrete walls)
- Doorway audio propagation

# Reflection
Developing this audio system was an invaluable learning experience that opened my eyes to a department I had previously overlooked during my academic career. Working with FMOD Studio changed my perspective on how game audio is designed and implemented.
The most significant challenge was understanding the complete pipeline from sound design to implementation. Initially approaching from a programmer's perspective, I had to adapt to think like an audio designer, considering factors like frequency balance, spatial positioning, and player psychology.
The manual FMOD integration taught me valuable lessons about engine architecture and plugin systems. While frustrating initially, this challenge forced me to understand the low-level connection between middleware and game engines.
Synchronizing footsteps with animations revealed the importance of precise timing in creating believable character audio. The solution required iteration and careful attention to frame-by-frame animation playback.
The reverb bleed issue taught me about signal processing and the importance of attack/release timing. Understanding how audio effects behave over time was crucial to creating smooth environmental transitions.
Overall, I'm satisfied with the results achieved within the project timeline. The artefact successfully demonstrates core audio programming concepts while providing an immersive player experience. While not matching AAA production quality, it effectively showcases the fundamental techniques used in modern game audio.
This project significantly improved my technical abilities and gave me deeper appreciation for sound designers' craft. The skills learned will be invaluable in future game development projects requiring audio implementation.

# Academic Context
**Institution**: <span style="color:Chartreuse">Anglia Ruskin University, Cambridge</span> \
**Course**: <span style="color:Chartreuse">BSc Computer Games Technology</span> \
**Module**: <span style="color:Chartreuse">MOD008619 - Technical Development for Games</span> \
**Element**: <span style="color:Chartreuse">010 - Audio Programming</span> \
**Academic Year**: <span style="color:Chartreuse">2023/24</span> \
**Grade**: <span style="color:Chartreuse">B</span>

# Links
<iframe frameborder="0" src="https://itch.io/embed/4109132" width="552" height="167"><a href="https://misdur.itch.io/audio-programming-prototype-documentation">Audio Programming Prototype - Documentation by Misdur</a></iframe>

---
*This project demonstrates my ability to integrate professional audio middleware with Unreal Engine, implement dynamic audio systems, and create immersive soundscapes that enhance player experience. It showcases both technical programming skills and understanding of audio design principles.*
