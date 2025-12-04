---
title: "**The Quantum Market**"
excerpt: '*A Unity card game demonstrating ScriptableObjects architecture for data management and procedural content generation*'
header:
    teaser: /assets/images/projects/quantum-market/qm-thumbnail.png
    overlay_image: /assets/images/projects/quantum-market/qm-banner.png
    overlay_filter: linear-gradient( rgba(0, 0, 0, 0.5), rgba(162, 0, 255, 0.5))
    actions:
        - label: "View on GitHub"
          url: "https://github.com/L-Pace/the-quantum-market"
        - label: "Download"
          url: ""

tags:
    - Unity
    - C#
    - Game Development
    - Procedural Generation
    - Card Game
    - Game Architecture
    - Scriptable Objects

date: 2024-12-01

gallery:
    - url: /assets/images/projects/quantum-market/screenshots/card.png
      image_path: /assets/images/projects/quantum-market/screenshots/card.png
      alt: "Card Prefab"
      title: "Card Prefab"

    - url: /assets/images/projects/quantum-market/screenshots/card-spec.png
      image_path: /assets/images/projects/quantum-market/screenshots/card-spec.png
      alt: "Card Specification"
      title: "Card Specification"

    - url: /assets/images/projects/quantum-market/screenshots/project-hierarchy.png
      image_path: /assets/images/projects/quantum-market/screenshots/project-hierarchy.png
      alt: "Project Hierarchy"
      title: "Project Hierarchy"

    - url: /assets/images/projects/quantum-market/screenshots/card-data-inspector.png
      image_path: /assets/images/projects/quantum-market/screenshots/card-data-inspector.png
      alt: "Card Data ScriptableObject in Unity Inspector"
      title: "Card Data ScriptableObject in Unity Inspector"

    - url: /assets/images/projects/quantum-market/screenshots/name-generator-inspector.png
      image_path: /assets/images/projects/quantum-market/screenshots/name-generator-inspector.png
      alt: "Name Generator ScriptableObject in Unity Inspector"
      title: "Name Generator ScriptableObject in Unity Inspector"
      
    - url: /assets/images/projects/quantum-market/screenshots/name-generator-config-inspector.png
      image_path: /assets/images/projects/quantum-market/screenshots/name-generator-config-inspector.png
      alt: "Name Generator Config ScriptableObject in Unity Inspector"
      title: "Name Generator Config ScriptableObject in Unity Inspector"


published: true
---

# Project Overview
![image-center](/assets/images/projects/quantum-market/qm-thumbnail.png){: .align-center}

The Quantum Market is a card-based game developed as my final university project for the Major Project for Games module at Anglia Ruskin University. This project demonstrates advanced implementation of Unity's ScriptableObjects architecture for managing game data and procedural content generation in a clean, maintainable, and designer-friendly way.
The game features a dynamic shop system where players can purchase procedurally generated cards with unique properties. Each card is created using a system of interconnected ScriptableObjects that manage card data, name generation, and market mechanics - showcasing modern game development architecture patterns.

**Development Time**: <span style="color:Chartreuse">2 months</span> \
**Team Size**: <span style="color:Chartreuse">Solo project</span> \
**Role**: <span style="color:Chartreuse">Programmer & Game Desisgner</span> \
**Platform**: <span style="color:Chartreuse">Unity</span> 

# Research Focus
This project was developed as part of an investigation into how ScriptableObjects can be effectively implemented in Unity game development, with particular focus on:

- **Data Management Architecture**: Separating data from game logic for better maintainability
- **Designer Workflow Enhancement**: Creating intuitive interfaces for content modification without code changes
- **Procedural Content Generation**: Dynamic card creation with unique properties and names
- **Rapid Prototyping**: Enabling quick iteration and testing of design changes
  
# Key Features
## 🃏 Dynamic Card System
- **Procedurally Generated Cards**: Each card features unique combinations of elements and stats
- **Five Element Types**: Plasma, Quantum, Neutron, Photon, and Dark Matter
- **Rarity System**: Different rarity levels that affect card statistics and value
- **Procedural Names**: Pattern-based name generation system creating unique card identities

## 🏪 Market Mechanics
- **Credit System**: Players start with 1000 credits for purchasing cards
- **Six-Card Market**: Shop displays six available cards at any time
- **Market Refresh**: Ability to generate new card offerings
- **Purchase Tracking**: Cards marked as purchased and added to collection

## 📊 Collection System
- **Player Collection**: Track and visualize all purchased cards
- **Persistent Data**: Collection maintained across game sessions
- **Card Statistics**: Detailed view of owned cards and their properties

# Technical Implementation
## ScriptableObjects Architecture
The core of this project is a three-tiered ScriptableObject system that demonstrates modern Unity architecture patterns:

### QuantumCardData ScriptableObject
```cs
using UnityEngine;

[CreateAssetMenu(fileName = "New Quantum Card", menuName = "Quantum Market/Card Data")]
public class QuantumCardData : ScriptableObject
{
    // Reference to NameGeneration ScriptableObject
    [Header("Name Generation")]
    [SerializeField]
    private NameGenerator nameGenerator;

    private string generatedName;

    [Header("Basic Info")]
    public string description;
    public Sprite cardArtwork;

    // Properties of the card including element type and rarity type
    [Header("Properties")]
    public QuantumEnums.ElementType elementType;
    public QuantumEnums.RarityType rarityType;

    // Different stats of the card
    [Header("Stats")]
    public int quantumPower;
    public int energyCost;
    public int creditCost;
    public bool isPurchased = false;

    /// <summary>
    /// This function is getting the name in case the card string
    /// is not null
    /// </summary>
    public string CardName
    {
        get
        {
            if (string.IsNullOrEmpty(generatedName))
            {
                GenerateCardName();
            }
            return generatedName;
        }
    }

    /// <summary>
    /// This funciont is creating the name of the card with the 
    /// NameGenerator. In case is null is producing a warning message
    /// inside of the console.
    /// </summary>
    public void GenerateCardName()
    {
        if(nameGenerator != null)
        {
            generatedName = nameGenerator.GenerateName();
        }
        else
        {
            Debug.LogWarning("Name Generator not assigned to card!");
            generatedName = "Unnamed Card";
        }
    }
}
```

This ScriptableObject manages all core card properties, organizing data into logical categories through header attributes. The separation between basic info, properties, and stats provides clear data organization while maintaining flexibility for runtime modifications.

### NameGenerator ScriptableObject
Manages procedural generation logic, interfacing between card data and configuration:

```cs
using UnityEngine;

[CreateAssetMenu(fileName = "Name Generator", menuName = "Quantum Market/Name Generator")]
public class NameGenerator : ScriptableObject
{
    // Reference to the NameGeneratorConfig ScriptableObject
    [SerializeField]
    private NameGeneratorConfig config;

    /// <summary>
    /// This function is generating the name with a specific
    /// pattern
    /// </summary>
    /// <returns>The pattern chose</returns>
    public string GenerateName()
    {
        // Check if the reference is null
        if (config == null)
            return "Unnamed Card";

        var pattern = SelectPattern();

        return FillPattern(pattern);
    }

    /// <summary>
    /// Default Select pattern, the designer can change it in the 
    /// inspector
    /// </summary>
    /// <returns>Return the the pattern on position 0 of the array</returns>
    private string SelectPattern()
    {
        if (config.patterns.Count == 0)
            return "{prefix} {noun}";

        float totalWeight = 0f;
        foreach(var pattern in config.patterns)
        {
            totalWeight += pattern.weight;
        }

        // Creating a random for the weight pattern
        float random = UnityEngine.Random.Range(0f, totalWeight);
        float currentWeight = 0f;

        foreach(var pattern in config.patterns)
        {
            currentWeight += pattern.weight;
            if(random <= currentWeight)
            {
                return pattern.pattern;
            }
        }

        return config.patterns[0].pattern;
    }

    /// <summary>
    /// This function is creating the name of the card
    /// </summary>
    /// <param name="pattern">Variable from SelectPattern funtion</param>
    /// <returns></returns>
    private string FillPattern(string pattern)
    {
        string name = pattern;

        if(config.prefixes.Count > 0)
        {
            name = name.Replace("{prefix}", config.prefixes[UnityEngine.Random.Range(0, config.prefixes.Count)]);
        }

        if(config.nouns.Count > 0)
        {
            name = name.Replace("{noun}", config.nouns[UnityEngine.Random.Range(0, config.nouns.Count)]);
        }

        if(config.suffix.Count > 0)
        {
            name = name.Replace("{suffix}", config.suffix[UnityEngine.Random.Range(0, config.suffix.Count)]);

        }

        return name;
    }
}
```
This ScriptableObject acts as a processor, transforming configuration data into meaningful card names while keeping generation logic separate from content.

### NameGeneratorConfig ScriptableObject
Provides the foundation for name generation by storing word lists and patterns:

```cs
using System.Collections.Generic;
using UnityEngine;

[CreateAssetMenu(fileName = "Name Generator Config", menuName = "Quantum Market/Name Generator Config")]
public class NameGeneratorConfig : ScriptableObject
{
    // Class for the name pattern 
    [System.Serializable]
    public class NamePattern
    {
        public string pattern;
        public float weight = 1f;
    }

    [Header("Word List")]
    public List<string> prefixes = new List<string>();
    public List<string> nouns = new List<string>();
    public List<string> suffix = new List<string>();

    [Header("Name Patterns")]
    public List<NamePattern> patterns = new List<NamePattern>();
}
```
The weighted pattern system enables controlled randomization, while separate word lists allow for easy content management and expansion.

### System Architecture Benefits
- **Modularity**: Clear separation between data storage, generation logic, and game behavior
- **Designer-Friendly**: All card properties and generation rules editable through Unity Inspector without code changes
- **Maintainability**: Well-organized project structure with logical folder hierarchy and clear naming conventions
- **Scalability**: Easy to add new card elements, rarities, and name generation patterns
- **Debugging**: Inspector-visible data makes it simple to track and modify values during development

# Technical Challenges & Solutions
## Challenge 1 - Managing ScriptableObject Dependencies

**Problem**: QuantumCardData depends on NameGenerator, which depends on NameGeneratorConfig - creating a dependency chain requiring careful setup

**Solution**: Implemented robust error handling and validation checks to ensure all references are properly assigned before runtime. Created clear documentation showing the dependency hierarchy and proper setup procedures.

## Challenge 2 - Card Display System
**Problem**: Cards were not displaying properly on the main canvas at game start despite correct instantiation logic

**Solution**: Restructured the card prefab to include a button component with an image overlay and explicitly set the localScale with Alpha 1. Ensured proper canvas scaling configuration in the CreateCard() function to prevent prefab settings from overriding scene canvas settings.

## Challenge 3 - Runtime Data Management
**Problem**: Balancing flexibility for dynamic card creation while maintaining data integrity of template cards

**Solution**: Implemented a system that separates template data (stored in ScriptableObjects) from instance data (runtime card state). The <span style="color:Red">isPurchased</span> boolean enables runtime state tracking without compromising underlying template data.

## Challenge 4 - Procedural Name Generation Balance
**Problem**: Ensuring generated card names were meaningful and not random gibberish

**Solution**: Developed a pattern-based generation system with weighted randomization. Separated word lists into prefixes, cores, and suffixes, allowing for controlled variety while maintaining coherent naming conventions.

# Code Architecture & Design Patterns
## Design Patterns Implemented
**Strategy Pattern**: Different card generation strategies based on element types and rarity levels

**Template Method Pattern**: Base card creation process with customizable steps for different card types

**Observer Pattern**: Event system for market updates and collection changes

**Factory Pattern**: Card instantiation and initialization through centralized creation methods

## Project Structure
```cs
Assets/
├── Scripts/ 
│   ├── ScriptableObjects/ 
│   │   ├── QuantumCardData.cs 
│   │   ├── NameGenerator.cs 
│   │   └── NameGeneratorConfig.cs
│   ├── Managers/ 
│   │   └── QuantumMarketManager.cs 
│   └── UI/ 
│       └── CardDisplay.cs 
├── ScriptableObjects/ 
│   ├── Cards/ 
│   ├── NameGenerators/ 
│   └── Configs/ 
├── Prefabs/ 
│   └── CardPrefab.prefab 
└── Scenes/ 
    └── MainMarket.unity
```

# Learning Outcomes
## Technical Skills Developed
**Unity Architecture**: Deep understanding of ScriptableObjects and their role in modern Unity development

**Data-Driven Design**: Learned to separate data from logic for better maintainability and designer accessibility

**Procedural Generation**: Implemented pattern-based content generation with controlled randomization

**System Design**: Created modular, interconnected systems that work together while remaining independent

## Game Development Insights
**Designer Empowerment**: Understood the importance of creating tools that allow designers to work independently from programmers

**Code Organization**: Learned the value of clear naming conventions, folder structure, and inline documentation

**Debugging Methodology**: Developed systematic approaches to solving complex UI and data management issues

**Architecture Planning**: Recognized the importance of planning system architecture before implementation to avoid costly refactoring

# Research Contribution
This project contributes to the understanding of ScriptableObjects in Unity through:

**Practical Implementation**: Concrete example of three-tiered ScriptableObject architecture

**Documentation**: Comprehensive technical report detailing implementation challenges and solutions

**Best Practices**: Demonstration of proper data organization and naming conventions

**Design Patterns**: Showcasing how traditional design patterns apply to Unity's component-based architecture

The research revealed that while Unity powers many successful games, technical documentation specifically about ScriptableObjects implementation is limited. This project helps fill that gap by providing a well-documented, practical example.

# Screenshots & Gameplay

{% include gallery caption="Some screenshots from Unity of The Quantum Market" %}


{% include video id="vEYRFziA-ms " provider="youtube" %}

# Future Improvements
If I were to expand this project, I would implement:
## Forge System
A crafting mechanic allowing players to combine cards to create new element types, demonstrating more complex uses of ScriptableObjects for dynamic content creation.

## Perks System
Player progression system with unlockable bonuses that affect card collection rates and credit generation, showing how ScriptableObjects can manage progression data.

## Enhanced UI/UX

- **Tooltips**: Hover information showing detailed card statistics
- **Visual Effects**: Particle systems and animations for card purchases and generation
- **Audio Feedback**: Sound effects for interactions and purchases

## Extended Card System

- **More Elements**: Additional element types with unique interactions
- **Card Abilities**: Special powers and effects for certain cards
- **Combo System**: Synergies between different card types in collection

# Technical Specifications

- **Engine**: <span style="color:Chartreuse">Unity 2022 LTS</span>
- **Programming Language**: <span style="color:Chartreuse">C #</span>
- **Architecture**: <span style="color:Chartreuse">ScriptableObjects-based data management</span>
- **Platform**: <span style="color:Chartreuse">PC</span>
- **Development Tools**: <span style="color:Chartreuse">Visual Studio, Unity Editor</span>
- **Version Control**: <span style="color:Chartreuse">Git with GitHub</span>

# Reflection
Developing The Quantum Market taught me valuable lessons about game architecture and the importance of planning data management from the start of development. The biggest insight came from separating the name generator from the configuration system - initially designed as one system, splitting them made the architecture clearer and more maintainable.
One of the most significant challenges involved understanding designers' needs, as I typically approach development from a programmer's perspective. This project pushed me to create systems that non-programmers could easily use and modify, improving my ability to design user-facing tools.
The card display challenge, though frustrating, taught me valuable lessons about Unity's UI system and the importance of attention to detail in prefab configuration. This experience improved my debugging methodology and deepened my understanding of how Unity's UI hierarchy interacts with ScriptableObjects.
Despite its challenges, I'm satisfied with what I achieved. The project successfully demonstrates the power of ScriptableObjects for creating maintainable, designer-friendly game systems. While currently a showcase of architecture patterns, I plan to expand it into a fully playable game incorporating the future improvements mentioned above.

# Academic Context
- **Institution**: <span style="color:Chartreuse">Anglia Ruskin University, Cambridge</span>
- **Course**: <span style="color:Chartreuse">BSc Computer Games Technology</span>
- **Module**: <span style="color:Chartreuse">MOD008624 - Major Project for Games</span>
- **Academic Year**: <span style="color:Chartreuse">2024/25</span>
- **Grade**: <span style="color:Chartreuse">A</span>

This project served as both a practical implementation and academic research into modern Unity architecture patterns, contributing to the broader understanding of data-driven game development.

# Links

- [GitHub Repository](https://github.com/L-Pace/the-quantum-market) - View complete source code
- Download the game, full development report and the technical documentation from Itch.io
  
<iframe frameborder="0" src="https://itch.io/embed/4092392" width="552" height="167"><a href="https://misdur.itch.io/the-quantum-market">The Quantum Market by Misdur</a></iframe>

---
*This project demonstrates my ability to architect complex game systems using modern Unity patterns, implement procedural content generation, and create designer-friendly tools while maintaining clean, maintainable code. It showcases both technical programming skills and understanding of game development workflows.*