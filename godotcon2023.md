---
theme: godot
paginate: true
marp: true
---

![bg left:40% 60%](assets/img/godot.png)

# **Super-charging content production with Godot addons**

Building a pipeline to predictable produce game content. 

---

![bg left:50%](assets/img/bitbrain-slide.png)
# @bitbrain

- working on a dwarven pixelart RPG! 💎⛏️
- maintainer of **pandora** and **beehave** 🐝
- loves Godot 💖🤖


---
# Godot's Design Philosophy

> New features from the core developers often focus on what will benefit the most users first.

source:
https://docs.godotengine.org/en/stable/getting_started/introduction/godot_design_philosophy.html

---
# Terminology

- **addon** = third-party code and assets (including plugins)
- **plugin** = a Godot editor plugin (requires `plugin.cfg`)
- **extension** = extends Godot's core via C++ through theGDExtension interface (requires `*.gdextension`)


---
# Plugins

Example: `addons/dialogic/plugin.cfg`
```
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

```
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




---

# Accellarate Prototyping
    Image: An artist's canvas with various game elements quickly added.
    Engagement: "Can anyone share an experience where an addon saved them significant time during prototyping?"
    Key Points:
        Highlight the strengths of addons: Rapid development, quick feature integrations, testing ideas swiftly.


---

# Creating a Content Pipeline

    Key Points:
        - integrations with critical gamedev tools & systems
        - debugging and developer consoles
        - mod support
        - custom importers

---
# Production Point Principle

    Image: A balanced scale with prototyping on one side and production on the other.
    Engagement: "Who here has shifted a game from the prototyping phase to production and felt the need to re-evaluate their tools and addons?"
    Key Points:
        Discussion on how the importance of tools and systems evolves from prototyping to production.

---



---

# Dangers of Over-relying on Addons in Large Projects

     Image: A game character walking on a rope bridge, with some planks (addons) looking unstable.
    Engagement: "Has anyone here faced a situation where an addon they relied on heavily was abandoned or started showing major issues during a crucial phase of development?"
    Key Points:
        The risk of dependencies on addons for major functionalities, especially in larger, long-term projects.

---

# The DIY Approach in Large Game Projects


---
# Questions?


![width:350px](./assets/img/bitbrain-discord.svg)

### youtube.com/@bitbraindev