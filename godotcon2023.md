---
theme: godot
paginate: true
marp: true
---

![bg left:40% 60%](assets/img/godot.png)

# **Super-charging content production with Godot addons**

Building a pipeline to produce game content predictably.

---

![bg left:50%](assets/img/bitbrain-slide.png)
# @bitbrain

- working on a dwarven pixelart RPG! 💎⛏️
- maintainer of **pandora** and **beehave** 🐝
- Godot = 💖

---
# Godot's Design Philosophy

> [...] new features from the core developers often focus on what will benefit the most users first.

source:
https://docs.godotengine.org/en/stable/getting_started/introduction/godot_design_philosophy.html

---
# Terminology

- **addon** = third-party code and assets (including plugins)
- **plugin** = a Godot editor plugin (requires `plugin.cfg`)
- **extension** = extends Godot's core via C++ through the GDExtension interface (requires `*.gdextension`)
- **module** = compiled with Godot's core

---
# Plugins

Example: `addons/dialogic/plugin.cfg`
```javascript
[plugin]

name="Dialogic"
description="Create dialogs, characters and scenes to display conversations in your Godot games.
https://github.com/coppolaemilio/dialogic"
author="Emi, Jowan Spooner, Exelia, and more!"
version="2.0-Alpha-10 (Godot 4.1.2)"
script="plugin.gd"
```

source:
https://github.com/coppolaemilio/dialogic/blob/main/addons/dialogic/plugin.cfg

---
# GDExtensions

Example: `addons/fmod/fmod.gdextension`

```javascript
[configuration]
entry_symbol = "fmod_library_init"
compatibility_minimum = 4.1

[libraries]
windows.editor.x86_64 = "res://addons/fmod/libs/windows/libGodotFmod.windows.editor.x86_64.dll"
windows.debug.x86_64 = "res://addons/fmod/libs/windows/libGodotFmod.windows.template_debug.x86_64.dll"
windows.release.x86_64 = "res://addons/fmod/libs/windows/libGodotFmod.windows.template_release.x86_64.dll"
```

source:
https://github.com/utopia-rise/fmod-gdextension/blob/master/demo/addons/fmod/fmod.gdextension

---

# Addon Ecosystem

Exploring the categories of Godot addons.
![bg right:50%](assets/img/asset-lib.png)

---

![bg](assets/img/addons.png)

---

# Workflow addons

Accellarate and automate common processes.

![bg right:60%](assets/img/cyborg.jpg)

---

![bg](assets/img/aseprite.png)

---


![bg](assets/img/aseprite-wizard.png)

---

# Integration addons

![bg left:50%](assets/img/ethernet.jpg)

Connect any tool directly into Godot Engine.

---

![bg right:52%](assets/img/fmod-studio.jpg)

# FMOD GDExtension

`utopia-rise/fmod-gdextension`

`alessandrofama/fmod-for-godot`

![width:300px invert](assets/img/fmod.png)

---


![bg left:40%](assets/img/balls.jpg)

![width:600px](assets/img/jolt-logo.svg)

Godot extension that integrates the Jolt physics engine.

`godot-jolt/godot-jolt`

<br/>

- works with `CharacterBody3D` and other familiar Godot nodes out of the box (drop-in replacement)


---

 # Feature extending addons

- show example of feature extending addons
- add image
---

# Template repositories

- show example of template repo addon
- add image

---
# Addon discovery

- Official: https://godotengine.org/asset-library
- Useful: https://github.com/godotengine/awesome-godot
- Goldmine: https://github.com/search?q=godot%2Baddon
- Supportive: https://itch.io/search?q=godot%2Baddon

---

# Content Pipelines

Building reliable workflows that produce content for your game.


---

# Task Complexity

| S | M | L | XL |
|---|---|---|----|
| fix translation | add new language | add voicelines | dialogue system |
| change color of sword| update sword animation|add new weapon type| itemization system|
| fix sound timing| add new sound effect| dynamic sound playback | integrating FMOD |
| fix level collision | rework existing level | add new level | procedural level generation |

---

# Identify the bottleneck

- Is the task a one-off?
- Does finishing the task create new work after?
- How much is human error a factor?
- Is it a common problem a lot of people solved before?

---

<center>

# Production Point Principle

### by 🖤 HeartBeast

<img class="avatar" src="assets/img/heartbeast.jpg">

</center>

---

# Accellarate Prototyping
    Image: An artist's canvas with various game elements quickly added.
    Engagement: "Can anyone share an experience where an addon saved them significant time during prototyping?"
    Key Points:
        Highlight the strengths of addons: Rapid development, quick feature integrations, testing ideas swiftly.
---

# Accellarate Production
    Image: An artist's canvas with various game elements quickly added.
    Engagement: "Can anyone share an experience where an addon saved them significant time during prototyping?"
    Key Points:
        Highlight the strengths of addons: Rapid development, quick feature integrations, testing ideas swiftly.
---


# There is no silver bullet

- the success of your game may be dependent on the quality of the addon
- building it yourself means you can own the design and architecture of it fully
- addons may get out of date and you will spend time trying to patch them yourself in case Godot updates
- debugging code that is not yours is often not fun and wastes a lot of time
- how can you be sure the addon code is performant and does what it says it does? What guarantees does the addon give you?

---

# Properties of a good addon

A **good** addon should be:

- useful
- well-documented
- tested
- **maintained** or **archived**
- compatible

---
# Questions?


![width:350px](./assets/img/bitbrain-discord.svg)

### youtube.com/@bitbraindev