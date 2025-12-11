---
title: "**Custom Toon Shader with Scriptable Render Pipeline**"
excerpt: "*Advanced shader system for stylized low-poly aesthetics using Unity's Shader Graph and custom render passes*"
header:
    teaser: /assets/images/projects/toon-shader/ts-thumb.png
    overlay_image: /assets/images/projects/toon-shader/ts-banner.png
    overlay_filter: linear-gradient( rgba(0, 0, 0, 0.7), rgba(162, 0, 255, 0.3))
    actions:
        - label: "View on GitHub"
          url: "https://github.com/L-Pace/toon-shader-project"
        - label: "Download"
          url: "https://spacegaminglab.itch.io/tooncel-shader-prototype"

tags:
    - Unity
    - C#
    - Game Development
    - Graphics Programming
    - URP
    - Non-Photorealistic Rendering
    - Shader Graphs

date: 2025-04-01

---

# Project Overview

{% include video id="iJ1Z8nYM2A0" provider="youtube" %}

This project investigates the implementation and artistic application of toon/cel shaders for low-poly 3D games using Unity's Universal Rendering Pipeline (URP). Through comprehensive research and technical development, I created a complete non-photorealistic rendering framework that combines Shader Graph for visual shader creation with custom C# scripts for advanced rendering features.
Inspired by the distinctive visual styles of games like *Hi-Fi Rush* and *Borderlands*, this shader system demonstrates how technical sophistication in rendering can complement geometric simplicity to create visually striking games with strong artistic direction.

**Development Time**: <span style="color:Chartreuse">1 month</span> \
**Team Size**: <span style="color:Chartreuse">Solo project</span> \
**Role**: <span style="color:Chartreuse">Graphics Programmer & Technical Artist</span> \
**Platform**: <span style="color:Chartreuse">Unity</span> 

# Research Focus
This investigation explores several key areas of non-photorealistic rendering:

**Technical Implementation**: How toon shading techniques can be implemented using modern Unity tools (Shader Graph, URP)

**Artistic Versatility**: Achieving different art styles within a cohesive low-poly aesthetic framework

**Visual Longevity**: Creating graphics that resist technical aging through stylization

**Shader Optimization**: Balancing visual quality with performance for low-poly games

**Custom Rendering**: Extending Unity's render pipeline for specialized effects

# Key Features
## 🎨 Advanced Toon Shader System
### Light Banding
- Quantized lighting into three distinct bands (full-light, mid-tone, shadow)
- Hard transitions between light levels for classic cel-shaded appearance
- Customizable band thresholds for different artistic styles
- Optimized for low-poly geometry with minimal light complexity

### Rim Lighting
- Enhanced edge definition highlighting object silhouettes
- Adjustable color, intensity, and width parameters
- Particularly effective on low-poly models, emphasizing geometric qualities
- Inspector-accessible controls for real-time artistic adjustments

### Material Properties
- Customizable base colors and tint options
- Specular highlights with controllable intensity
- Shadow color control for artistic expression
- Support for texture-based variations

## 🖼️ Custom Outline System
### Hybrid Outline Approach
- Combination of normal-based and depth-based edge detection
- Consistent rendering across varied geometry types
- Addresses challenges specific to low-poly models with sharp edges
- Adjustable outline thickness and color

### Post-Processing Integration

- Implemented as custom render feature in URP
- Processes entire scene for unified outline style
- Better performance than traditional vertex extrusion methods
- Maintains outline consistency during camera movement

## Custom Bloom Effect (Hi-Fi Rush Style)
### Scriptable Render Pipeline Implementation

- Three custom C# scripts extending Unity's URP
- Multi-pass Gaussian bloom with down-sampling and up-sampling
- Texture-based masking instead of camera-based application
- Superior artistic control compared to Unity's standard bloom

### Customizable Parameters
- Threshold control for bloom activation
- Intensity adjustment for effect strength
- Scatter control for bloom spread
- Color tint for stylistic variations
- All parameters exposed in Unity Inspector

# Technical Implementation
The core toon shader uses node-based visual programming in Shader Graph:

```bash
Main Shader Pipeline:
├── Light Calculation
│   ├── Dot Product (Normal · Light Direction)
│   ├── Step Function (Quantization)
│   └── Band Thresholds (3 levels)
├── Rim Lighting
│   ├── View Direction Calculation
│   ├── Fresnel Effect
│   └── Rim Intensity Control
├── Color Processing
│   ├── Base Color Application
│   ├── Shadow Color Blending
│   └── Specular Highlights
└── Output
    └── Surface Shader Output
```