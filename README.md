# Haunted-Brain   Digital-Prototype

## Table of contents
- [About the Project](#About-the-project)
- [Game Design Document](#Game-Design-Document)
- [Gameplay Demo](#Gameplay-Demo)
- [Play the Prototype](#Play-the-Prototype)
- [Making Of](#Making-of)
- [Credits](#Credits)

## About the project

This project's goal was to develop a digital prototype building on a prior project, in which the initial game concept and Game Design Document (GDD) were created.

## Game Design Document

### Summary

Haunted Brain is a hybrid of an open-world exploration game and a fast-paced platformer where players help young Jack overcome his irrational fears inside a mysterious mansion. While exploring freely in third-person, Jack occasionally enters nightmare-like chase levels in which he must escape terrifying monsters through skill-based platforming sections. Completing these levels rewards experience points that can be invested in the **Fear Mastery** skill tree, gradually increasing Jack's resistance to fear until he overcomes all of his anxieties. In addition to the main story, the game features optional challenge modes where players can either hunt children as a monster or survive endless nightmare encounters while competing for high scores.

### Table of Contents
- High Concept
- Moodboards
- Characters
- Core Loop
- Mechanics
- Set of rules
- Level Design/Game Session
- UI
- Tutorial
- Sketches
- Business Model


*If you are interested in reading the GDD feel free to [contact me](mailto:mariobannert96@gmail.com)*



## Gameplay Demo

[![Gameplay Video](https://img.youtube.com/vi/x5oyTqKHVds/maxresdefault.jpg)](https://youtu.be/x5oyTqKHVds)

*Click the image to play the video*

## Play the Prototype
[Play on itch.io](https://mol96.itch.io/haunted-brain-prototype)<br>
Password: HauntedBrain

*Windows build – download, unzip, and run the .exe*

## Making Of

The prototype is built around an example gameplay session that also functions as a tutorial. Development relied heavily on internet tutorials, adapted to fit this specific project. Visual and atmospheric polish was achieved using Asset Store assets along with animations and the character model from Mixamo. The main focus, however, was on implementing core functionality level design and correct script usage.

### 1. Main Menu

For the main menu, I created a dedicated scene with a canvas containing buttons. The "Play" button uses a scene-switching script to transition into the next scene, the house, while "Quit" closes the game. An additional camera, stacked with the main camera, renders the particle systems that create a fog effect along the screen edges.


<img width="753" height="424" alt="Main_Menu" src="https://github.com/user-attachments/assets/a9d4b8aa-d673-4d87-a713-a3adea95c3d1" />




### 2. The House

After the scene loads, the player finds themselves as Jack in his childhood bedroom. Building the house took the most time overall. I created the base structure in Blender, along with the stairs, which I fitted with plane colliders in Unity to ensure smooth movement. The work also involved writing scripts, setting up lighting, animations, sound, and adding colliders to interactive objects. Given the time it would have taken to model every object myself, I opted to use Asset Store assets instead. For Jack and Martha's voices, I recorded original voice lines with my girlfriend to make the scene feel more alive.

After accepting the task inside the house, the player heads to the basement, opens the door, and triggers a transition into the next scene.


<img width="753" height="424" alt="The_House" src="https://github.com/user-attachments/assets/f34a1d8a-6e49-42df-b390-3fd653556f24" />




### 3. Loading Screen and Endless Runner

Triggering this transition leads to the next scene, the loading screen, from which pressing the spacebar takes the player into the Endless Runner. I deliberately split the experience into several smaller scenes to keep the project organized and manageable.

A script randomly assembles the level from 3 sections, building it up piece by piece as the player progresses. Colliding with an obstacle triggers a message and gives the player the option to restart the level. After 20 seconds, the level's active ability becomes available a flashlight that lets the player gain distance from the fog. The fog's hands were created in Nomad Sculpt and Blender. After 60 seconds, the level ends automatically and transitions to the next scene.

<img width="753" height="425" alt="Loading_Screen" src="https://github.com/user-attachments/assets/42051e54-eef5-41b7-89f3-526c5e510346" />

<img width="753" height="424" alt="Endless_Runner" src="https://github.com/user-attachments/assets/b98644b3-f384-44be-8600-df12642418db" />



### 4. Back in the House

The player then returns to the house, this time in the basement a new scene rather than the same one from Scene 2. This is because I wanted certain changes to the house to only become visible after completing the level. Opening the skill tree, now located in Jack's room, simulates distributing the XP earned during the level. This is displayed via a video player texture rendered on a canvas. Closing the skill tree leads to an end screen, concluding the session.


<img width="755" height="427" alt="Skill-Tree" src="https://github.com/user-attachments/assets/91eebe54-73ea-4947-8958-23a8da0808e1" />



## Credits

### Jack & Animations:<br>
- Character model: "Aj" from [Mixamo](https://www.mixamo.com/#/?page=1&type=Character)<br>
- Character animations from [Mixamo](https://www.mixamo.com/#/?page=1&type=Motion%2CMotionPack)<br>
- Voice: Mario B.

### Martha & Animations:<br>
- Character model: "Elizabeth" from [Mixamo](https://www.mixamo.com/#/?page=1&type=Character)<br>
- Character animations from [Mixamo](https://www.mixamo.com/#/?page=1&type=Motion%2CMotionPack)<br>
- Voice: Sophia K.

### Textures
- Metall_0058 - TextureCan, [texturecan.com](https://www.texturecan.com/details/475/)
- Plastered Wall - Amal Kumar, [PolyHaven](https://polyhaven.com/a/plastered_wall)
- Wood_067 - Ambientcg, [ambientcg.com](https://ambientcg.com/view?id=Wood067)

### Props (Unity Asset Store)
All by Geniuscrate Games:
- [Bathroom Set-Interior](https://assetstore.unity.com/packages/3d/props/furniture/bathroom-set-interior-263462)
- [Kitchen Set-Interior](https://assetstore.unity.com/packages/3d/props/furniture/kitchen-set-interior-263284)
- [Bedroom Set-Interior](https://assetstore.unity.com/packages/3d/props/furniture/bedroom-set-interior-264498)
- [Table Set-Interior](https://assetstore.unity.com/packages/3d/props/furniture/table-set-interior-263303)

### Scripts (Tutorials & References)
- Doors, PickUpItems - User1 Productions, [Google Drive](https://drive.google.com/drive/folders/1dAGsuK8YghYfqNv4CE773wSaRxIRlQZw)
- CameraHolder, PlayerCam & PlayerMovement - Dave/GameDevelopment, ["First Person Movement in 10 Minutes"](https://www.youtube.com/watch?v=f473C43s8nE&t=346s)
- PlayerMove, ObstacleCollision, EndRunSequence, GenerateLevel, LevelBoundary – Jimmy Vegas, ["Endless Runner Tutorials in Unity - Old Series"](https://www.youtube.com/playlist?list=PLZ1b66Z1KFKit4cSry_LWBisrSbVkEF4t)

### Sounds
- PickUp, DoorOpenSound – User1 Productions, [Google Drive](https://drive.google.com/drive/folders/1RVNi_Pn8_n22tXM_DVDLHoy_nuXJm4s4)
- SteppingOnTile_01, Dark Tension Music – User1 Productions, [Google Drive](https://drive.google.com/drive/folders/1Hp5EAu3GFToa8WHeAfwVwrIBZUvzUBRU)
- Monster Chase Grunts - freesound_community, [Pixabay](https://pixabay.com/de/sound-effects/monster-chase-grunts-45476/)
- Thunder/Lightning- II - Without Rain / Wind / Background noise. - GregorQuendel_SoundDesign, [Pixabay](https://pixabay.com/de/sound-effects/natur-thunder-lightning-ii-without-rain-wind-background-noise-136312/)
- Rain - Falling on a wooden roof. - GregorQuendel_SoundDesign, [Pixabay](https://pixabay.com/de/sound-effects/natur-rain-falling-on-a-wooden-roof-137242/)
