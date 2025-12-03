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
          
tags:
    - Unreal Engine 5
    - Game Development
    - Solo Project
    - Blueprints
    - Audio Programming
    - FMOD
    - Prototype

date: 2023-04-25

gallery:
    - url: /assets/images/projects/audio-programming/Screenshots/screenshot-1.png
      image_path: /assets/images/projects/audio-programming/Screenshots/screenshot-1.png
      alt: "Logic Track - Grass"
      title: "Logic Track - Grass"

    - url: /assets/images/projects/audio-programming/Screenshots/screenshot-2.png
      image_path: /assets/images/projects/audio-programming/Screenshots/screenshot-2.png
      alt: "Fader"
      title: "Fader"

    - url: /assets/images/projects/audio-programming/Screenshots/screenshot-3.png
      image_path: /assets/images/projects/audio-programming/Screenshots/screenshot-3.png
      alt: "Big Room Int"
      title: "Big Room Int"

published: true
---

# Project Overview
![image-center](/assets/images/projects/audio-programming/Screenshots/Picture1.png){: .align-center}
This project is one of the assignments for university on my attempt to create a prototype on audio programming using Unreal Engine 5.2 and FMOD Studio. The prototype showcases the integration of the middleware in the graphic engine. 

**Development Time**: <span style="color:Chartreuse">2 months</span> \
**Team Size**: <span style="color:Chartreuse">Solo project</span> \
**Role**: <span style="color:Chartreuse">Programmer & Game Desisgner</span> \
**Platform**: <span style="color:Chartreuse">Unreal Engine 5.2</span> \
**Middleware**: <span style="color:Chartreuse">FMOD Studio</span>

# Screenshots
{% include gallery caption="Some screenshots of FMOD" %}
 
# Introduction
Audio Programming is a fundamental aspect of the computer games industry, playing an important
role in enhancing the immersive experience of interactive virtual environments. In this academic
research, we explore the complexities of audio programming in the context of computer games,
including the theoretical basis and practical implementations.
A key component of audio programming in games is the use of tools and APIs designed specifically
for real-time audio processing. These tools, which include FMOD Studio from Firelight (Firelight,
2024), Wwise from Audiokinetic (Audiokinetic, 2024), and OpenAL (OpenAL, 2024), give
developers a range of features for dynamic mixing, spatial audio rendering, and the development of
interactive sound effects.
In computer games, sound design goes beyond simple sound aesthetics to function as a dynamic
element deeply interconnected with gameplay mechanics and narrative development. To improve
player immersion and engagement, audio programming makes it possible to create interactive
soundscapes, adaptive music systems, and spatialized audio cues.
The integration of complicated audio functionalities into game development pipelines is made easier
by middleware solutions, which include proprietary and third-party audio engines. Examining the
integration of audio middleware platforms, such as FMOD Studio and Wwise, shows complex audio
production workflows and adaptive audio strategies designed for interactive gaming environments.

## The Artefact
In this research, I created an artefact that shows different sounds that correspond to various surfaces in
a third-person survival/exploration game.
The sound of the steps changes depending on the type of
surface the main character is running on—three different kinds of surfaces. The sounds that are used
to simulate footsteps are grass, wooden floors, and regular/paved surfaces. The sound of the wooden
floor steps is altered by the addition of a vast reverberant room, and there is an ambient cue for the
lightbulb buzzing inside. I also included some birds chirping as background noise in case the player
runs towards the grass. The sounds of the birds are still audible from the large room, although at a
reduced loudness.

## Aims and Objectives
With this demo, I intended to provide the player with a far more engaging experience. I believe that
the player has to experience the surroundings, not just the ambience but also the sense of being in a
real-world living scenario. Creating a main character who respects real-world sounds is one of the
first stages towards giving the player an immersive experience. To move around the gaming
environment, the main character must run or walk. However, merely moving without making noise
does not provide the player with the minimum experience necessary to enjoy the game. Therefore, I
have implemented a system that simulates the sounds of footsteps on multiple surfaces.
A nice representation of it is the large room in this demo. As the player enters this large, empty room,
they will notice a change in the sound of their footsteps due to the room's natural reverberation. The
player can still hear the birds chirping, but they are a little muted and less loud due to the wall.
The room also has a nice cue that simulates a humming lightbulb in the background, which improves
the player's experience even more.
The player can hear and feel the birds chirping on the grass surface, even from a distance. They can
also feel the sound of the birds progressively getting louder and quieter as they move away from the
area.
Any type of third-person video game, such as shooter, exploration, survival, and role-playing games,
can use these improvements.

# Background and Context
## Immersive Worlds
The current high standards set by players in the video game business are pushing development teams
to create games with ever-higher levels of gameplay complexity and, more importantly, user
immersion.
By enhancing the Diegetic Setting with audio, the developers aim to create the most immersive
environment possible between the player's empathy and the world setting (Huiberts, 2010, pp. 93-95).
Video games require an immersive environment that aims to improve the player's experience. The
goal of games like *Ghost of Tsushima* (Sucker Punch Production, 2020), *Red Dead Redemption 2*
(Rockstar Games, 2018), *Subnautica* (Unknown Worlds Entertainment, 2014) and *No Man’s Sky*
(Hello Games, 2016) is to make the player feel like they are a part of the environment and that it
responds to their initiatives.
How are they going to accomplish that?
In immersive worlds, sound design is crucial. The player should be able to hear their footsteps, hear
something moving in the dark, or even just hear a tool breaking a rock to feel completely immersed in
the environment. Ambience cues are particularly important in immersive worlds because they are
responsive and not just static examples of the environment. For instance, in a big city, the player may
hear a siren in the distance. This siren may alert the player to a change in the surroundings, or it may
simply be the result of an action the player has performed (Bridget, 2007).
We can see examples of how sounds can enhance immersion in each of the previously mentioned
video games.

## Cases of Study
### Ghost of Tsushima
In *Ghost of Tsushima*, the player controls the main character, Jin Sakai. He must produce different
sounds on different surfaces, such as grass, rocks, dirt (RedSonic01, 2022), wood floors
(GamingIsFun, 2020), and other sounds associated with movement. Thanks to the various ambience
cues that respond according to the character's location, such as birds chirping, various adjacent forest
sounds, or even the sound of the wind moving grass or vegetation, he is fully immersed in the world.

### Red Dead Redemption 2
In *Red Dead Redemption 2*, the player explores an extremely immersive environment where every
sound is thought to improve the whole experience. Everything in the game features superb ambient
cue placement designed by the developers specifically for this open-world Western game. Starting
with sounds from the forest, moving on to boats peacefully navigating a river, and ending with
ambient sounds from the town, such as dogs barking and animals moving in groups (Matthew Lee,
2020).

### Subnautica
*Subnautica*, in contrast with the last two games discussed, is a first-person survival game set on an
alien planet where the player character finds themselves stranded. The game's immersive atmosphere
is crafted through ambient sounds that deeply immerse the players in the underwater environment.
Whether inside their base or exploring the surroundings, players can distinctly hear the creatures
nearby, with sounds ingeniously manipulated to evoke the sensation of being underwater (Silent
Rabbit Gaming, 2022). Moreover, players can notice that the main character's footsteps sound change
depending on the surface they walk on (Silent Rabbit Gaming, 2022).

### No Man's Sky
Another great example of how the game's sounds have been included to enhance the player experience
is *No Man's Sky*. The sound of the player's footsteps changes according to the surface they are
walking on (NoloPada, 2023), just like in previous games, but the spaceship cockpit experience is
unquestionably the most immersive part of the game (robingood21century, 2024). The sound of the
wind hitting the windscreen and the cracking of the cockpit under air pressure allows the player to
experience the spaceship's velocity in addition to its visual features. The cockpit's cracking sound cue
is an extremely important feature because it gives the player the feeling that something is unstable and
unreliable, making them on alert in case a sudden malfunction strike.

# Approach
After researching the games I discussed in the Background Section of this essay, I decided to take a direct approach to the topic. The artefact includes ambient sounds and dynamic footsteps for the main character that corresponds to the different surfaces they walk on. I choose to use FMOD Studio as middleware with Unreal Engine 5.2 in order to accomplish this.

## Creating the Audio with FMOD Studio
FMOD Studio is an extremely powerful middleware application that provides game developers with a
more efficient and well-organized way of modelling and importing audio into their games. I used the
free samples that FMOD Studio had included for this attempt.

## Character Footsteps
Making specific Events suited to our requirements should be our primary objective. Regarding
footsteps, I made the event Footsteps (**Figure 1**) and put it into the previously made Bank PlayerSFX (**Figure 2**).

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-1.png){: style="width:500px" .align-center}
<p style="text-align:center;"><i><b>Figure 1: </b></i> <i>Footsteps Event</i></p><br>

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-2.png){: style="width:500px" .align-center}
<p style="text-align:center;"><i><b>Figure 2: </b></i> <i>Player/Footsteps attached to PlayerSFX
Bank</i></p><br>

I made four separate audio tracks inside of the timeline in order to put together the sounds that we needed for our player's footsteps (**Figure 3**). I used three distinct sounds from the same family in each of them. I utilised three distinct sounds to simulate footsteps on grass for the 'grass sound', and to add realism, I included a Random post-processing effect that modifies the volume and pitch of each track (**Figure 4**).

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-3.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 3: </b></i> <i>Timeline with all the footsteps sound</i></p><br>

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-4.png){: style="width:600px" .align-center}
<p style="text-align:center;"><i><b>Figure 4: </b></i> <i>Random Post-process effect on Volume and Pitch</i></p><br>

I also created a second Actionsheet, SurfaceType, to which I added Automation for the Volume of
each track (**Figure 5**). Additionally, I added a 3-EQ Post-process effect to the grass to change the sound of the footsteps (**Figure 6**). The SurfaceType sheet shows that we have a number of
automations for the volume. It is evident that the Grass track begins at 1 dB, while the remaining
tracks are at 0 dB. This implies that the first track will always be played in the event that the timeline value stays the same. Additionally, we can see that when the value 1 appears on the timeline, the red line changes to 0 dB, and so on. We will adjust the sound depending on the different materials by using these values in Unreal Engine settings later.

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-5.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 5: </b></i> <i>SurfaceType</i></p><br>

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-6.png){: style="width:800x" .align-center}
<p style="text-align:center;"><i><b>Figure 6: </b></i> <i></i>Grass Automation Volume and 3-EQ</p><br>

### Ambience Sounds
I choose to use the sound of birds chirping from FMOD studio's sound library for the ambience
sounds. In this instance, I used a Timeline to create an Audio track and added a scattered instrument to it. I have now included five distinct tracks with various bird sounds (**Figure 7**). I added two random effects for pitch and volume to the audio to make the result more realistic. At last, I made a small adjustment to the Scatter Distance and Spawn Interval (**Figure 8**).

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-7.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 7: </b></i> <i>Birds Chirping sounds</i></p><br>

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-8.png){: style="width:800x" .align-center}
<p style="text-align:center;"><i><b>Figure 8: </b></i> <i>Settings for the Birds Chirping</i></p><br>

### The Big Room
I added a lightbulb buzz/hum sound within the big room in the playing area's corner. I followed the
same procedure as before to add the track to the timeline (**Figure 9**), but this time I avoided any post-process effects.

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-9.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 9: </b></i><i>Lightbulb buzz/hum track</i></p><br>

### Define Internal and External Sounds
I had to make multiple groups in the mixer and give the appropriate sound to each group to determine whether a sound was intended for internal or external ambience. I can fully independently control the sounds that are specific to each group in this way. We also have a Return (Rtn) node, which I named BigRoom; this serves as our internal ambience sound's reverb (**Figure 10**).

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-10.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 10: </b></i><i>Mixer</i></p><br>

As we can see, the Return BigRoom and the internal ambience (AmbienceInt) have default volumes
of 0 dB (Figure 10). This is happening because we require the reverberation to be present just while our character is in the Big Room. I made a Snapshot in the Snapshot tab to accomplish this (**Figure 11**).

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-11.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 11: </b></i><i>Snapshot of AmbienceInt</i></p><br>

## Unreal Engine and FMOD Studio
In Unreal, the initial step is to add the physical surfaces to the Engine (**Figure 12**).

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-12.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 12: </b></i><i>Physical Surface</i></p><br>

We have the logic to define when the player is walking on a specific surface inside the character's
animation blueprint. In the function Play Event 2D we will find the Footsteps event from FMOD
Studio created before (**Figure 13**). Notification points applied to the animation are what trigger the sounds of the character's footsteps (Figure 14).

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-13.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 13: </b></i><i>Character Animation Blueprint</i></p><br>

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-14.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 14: </b></i><i>Footsteps notifies</i></p><br>

The final step is to create the game's actual surface and choose the desired material from the Phys
Material Override (**Figure 15**)

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-15.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 15: </b></i><i>Footsteps notifies</i></p><br>

To add the sound of birds chirping (**Figure 16**) and lights buzzing/hum to the scene, simply drag and
drop the cue from the FMOD folder in Unreal Engine (**Figure 17**).

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-16.png){: style="width:800px" .align-center}
<p style="text-align:center;"><i><b>Figure 16: </b></i><i>Birds Chirping Ambience Cue</i></p><br>

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-17.png){: style="width:600px" .align-center}
<p style="text-align:center;"><i><b>Figure 17: </b></i><i>The actual bird chirping from FMOD found in the Unreal Engine Folder</i></p><br>

# Artefact Outcomes
## Challanges Faced
### Installing FMOD in Unreal Engine 5.2
The integration of FMOD into Unreal Engine 5.2 was without a doubt the first challenge I
encountered while working on this artefact. Unfortunately, there is not a market-downloadable plugin for Unreal, so I had to install FMOD manually.
After downloading FMOD Studio, I dragged and dropped each of the folders from the zip file into the
Unreal Plugins folder that I had previously made. As a result, Unreal Engine was able to identify the plugin, and I had to manually correct a few of the issues that came up. The simplest method was to start a new project in FMOD Studio and integrate it with my Unreal project; this allowed me to resolve every issue that had been lifted in Unreal. To get everything set up and operational for the implementation of my artefact, the next step was to build a Bank and link it in Unreal.

### Synchronising the Animations with the Footsteps Sounds
The synchronisation of the mannequin's animation with the footsteps sound presented another
challenge for me. I had to make a new notification track on the running animation and select the right spot for the new notifications, as seen in Figure 15. Initially, I saw that the sounds were occasionally triggered. I resolved this by adding a notification to each of the "L" and "R" notifications for the whole animation montage.

### Internal Ambience Sounds
I found some difficulties configuring FMOD's internal ambience sounds correctly. Even outside the
Big Room, I could continue to hear the reverberation. In any case, the problem was initially evident because it took the reverb two and a third seconds to deactivate after leaving the Big Room. The best I could do by adjusting the Attack and Release of the reverb inside the Snapshot was to shorten the time to roughly one second after exiting the Big Room (**Figure 18**).

![image-center](/assets/images/projects/audio-programming/Screenshots/figure-18.png){: style="width:600px" .align-center}
<p style="text-align:center;"><i><b>Figure 18: </b></i><i>Snapshot Reverb - Attack and Release</i></p><br>

## Artefact Strength
The successful implementation of the many sounds that are improving the player's experience is one
of the artefact's strengths.
The outcome of the grass surface and the sound of the birds chirping particularly satisfied my
expectations. One of the artefact's strengths, in my opinion, is the proximity cue provided by the birds' chirping within the external ambience sounds. Additionally, the Big Room's well-designed reverb and buzzing light bulb give the player the impression that they are in an empty space with just their footsteps and the lightbulb's hum sounds.
One more strength is the sound of birds chirping within the Big Room. The player gets the sensation
that the sounds traverse the wall and get softer if they are getting closer to the wall next to the cue placed outside.
Another plus of this artefact is the seamless transition between the sounds of various surfaces. I put two different surfaces quite close to one another, as we can see in the video demo I presented, and we can hear how the noises instantly change depending on the surface, including the default surface.

## Design Choice
It is obvious that the video game *Ghost of Tsushima* inspired my design decision regarding the main character's footsteps and ambient sounds. I concentrated my research on this game since, from my experiences with it, I could see that the developers went above and beyond to provide the most
immersive experience possible for the player. I was so thrilled with the way the sounds in the game
were layered upon one other artistically that I wanted to try and replicate some of the key elements of the experience.
Although I am conscious that my attempt is not as good as that of a whole development team with
years of experience, I believe that I was able to approximate some of the game's elements.
Nevertheless, I am generally happy with the way the artefact turned out.

# Conclusion and Reflection
## Reflection on Project and Artefact Development
During the development of my artefact, I faced both successes and challenges that contributed to my
learning experience. In consideration of all the concepts presented in the introduction, I believe I achieved a satisfactory outcome overall, and therefore, I can consider improvements for future
implementations.

### Successes and Achievements
Throughout the development process, I successfully implemented the design choices and features
outlined in my project proposal. The artefact, which takes inspiration mostly from *Ghost of Tsushima*, successfully integrates elements of the game's atmosphere and, for the objective of this attempt, offers the player an immersive experience.
Moreover, integrating and implementing the audio in Unreal Engine with the assistance of FMOD
was one of my greatest accomplishments. Finding out how the two systems worked changed my
perspective on a department that I missed entirely during my academic career until now.

### Challenges and Lessons Learned
Even though I was successful, there were still several challenges I had to overcome while developing the artefact. As I previously mentioned, a big challenge was the integration of FMOD into Unreal Engine manually because there are no first-party plugins available.
An additional significant challenge for me was dealing with the complexity of the ambience and
footsteps sound integration, particularly in terms of optimising their application within the artefact.
This challenge made clear how crucial it is to do more in-depth research and preparation in the early stages of development in order to anticipate potential challenges and limit the risk that the project will fail to be delivered within the deadline.
In addition, I had challenges with feature prioritisation and scope management. I also realised that I felt inspired to add features or design elements outside the project's initial ideas, which could have caused scope creep and delays. With the aid of hindsight, I can now see how crucial it is to stick to the project's defined goal and scope.

### Future Considerations and Areas for Improvement
My goal for upcoming projects is to better plan and prioritise the various tasks and organise the
development process.
Furthermore, doing more in-depth research will improve my learning experience and certainly
contribute to my success in the industry.
Implementing additional features that I removed from the original design will be a good improvement
for the artefact in the future. I would like to incorporate music, for instance, that will give the player an even more immersive and interactive experience with the video game.

## Conclusions
In conclusion, creating my artefact has been an invaluable educational experience that has allowed me to dive into a new aspect of the video game industry and gain insight into both my areas of strength and growth as a student.
By reflecting on both successes and challenges experienced, I am better prepared to address future
projects with a more strategic approach. I am going to put everything I have learnt along the way into practice as I continue to develop as a technical and creative professional in the video games industry.

# References

- Audiokinetic (2024) Wwise. Available at: [Wwise](https://www.audiokinetic.com/en/wwise/overview)
(Accessed: 27 April 2024).
- Bridget, R. (2007) ‘Interactive Ambience’. Game Developer, 14(4), pp. 36.
- Firelight (2024) FMOD Studio. Available at: [FMOD-Studio](https://www.fmod.com) (Accessed: 27 April 2024).
- GamingIsFun (2020) ‘GHOST OF TSUSHIMA - 100% Walkthrough No Commentary - Part 1 [PS4
PRO]’. Available at: [YouTube](https://youtu.be/i72Amz98gxY?si=etHCUzsNcMXgjtJ6&t=720) (Accessed: 26 April 2024).
- Hello Games (2016) No Man’s Sky. Available at: [Hello-Games](https://www.nomanssky.com) (Accessed: 27 April 2024).
- Huiberts, S. (2010) Captivating sound - The role of audio for immersion in computer games. PhD
Thesis. Utrecht School of the Arts (HKU) and University of Portsmouth (UK). Available at: [PhD-Thesis](https://download.captivatingsound.com/Sander_Huiberts_CaptivatingSound.pdf) (Accessed: 26 April2024).
- Matthew Lee (2020) ‘RDR2 Composition & Sound Design/Foley’ Available at: [YouTube](https://www.youtube.com/watch?v=RSJqKpGLK8s) (Accessed: 26 April 2024).
- NoloPada (2023) ‘No Man's Sky Chill Gameplay 1 (Relaxation, Sleep, Study) [No Commentary]’.
Available at: [YouTube](https://youtu.be/hztJfTjWdi0?si=p8d3ftpRxlEB57do&t=98) (Accessed: 26 April 2024).
- OpenAL (2024) OpenAL. Available at: [OpenAL](https://www.openal.org) (Accessed: 27 April 2024).
- RedSonic01(2022) ‘Ghost of Tsushima, SFX only, Foley Walk Jump Roll Run’. Available at: [YouTube](https://www.youtube.com/watch?v=M0_BHepCZ-s) (Accessed: 26 April 2024).
- robingood21century (2024) ‘No Man's Sky 2024. Exploration ULTRA GRAPHICS. No commentary
gameplay 4K | 60 FPS’ Available at: [YouTube](https://youtu.be/h8qHqP3JYxs?si=CgeLZxgr5wT1H9xY&t=75)
(Accessed: 26 April 2024).
- Rockstar Games (2018) Red Dead Redemption 2. Available at: [Rockstar-Games](https://www.rockstargames.com/reddeadredemption2) (Accessed: 27 April 2024).
- Silent Rabbit Gaming (2022) ‘Exploring The Aura | Subnautica | No Commentary | Part 8’. Available
at: [YouTube](https://youtu.be/4BpR6y6fEr8?si=M65YXJWSCH2N-VvA) (Accessed: 26 April 2024).
- Silent Rabbit Gaming (2022) ‘Exploring An Alien Facility | Subnautica | No Commentary | Part 14’.
Available at: [YouTube](https://youtu.be/CCrwyUh3OtI?si=gFEyVLe3ACDzhqWg&t=1207) (Accessed: 26 April
2024).
- Sucker Punch Production (2020) Ghost of Tsushima. Available at: [Sucker-Punch-Production](https://www.suckerpunch.com/category/games/ghostoftsushima/) (Accessed: 27 April 2024).
- Unknown Worlds Entertainment (2014) Subnautica. Available at: [Unknown-Worlds-Entertainment](https://unknownworlds.com/subnautica/) (Accessed: 27 April 2024).

# External Assets
For this project, I used 3 free materials from Quixel:

- Cut_Grass_sfenffsa_4K
- Old_Carpet_vddldbw_2K
- Wooden_Floor_whnfeb2_2K_Mat

For the sounds, I used the samples integrated in FMOD Studio.
I followed these tutorials:

- [Let's Add Sound (with FMOD and Unreal)](https://youtu.be/tCMb8mJqB4A?si=MSx4EPFNWEzgM33Q)
- [FMOD Studio Tutorial - How to Create Adaptive Audio for Video Games](https://youtu.be/7A1HMOsD2eU?si=fwXu_2NW4fmEGDyY)
- [FMOD & Unreal Engine 5: Integration](https://youtu.be/w_cjlfkEnVQ?si=hNr5OPGVsYYHcgsB)