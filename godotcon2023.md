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

- German based in the UK
- working on a dwarven pixelart RPG! 💎⛏️
- maintainer of **pandora** and **beehave** 🐝
- Godot = 💖

<center style="margin-top:80px; font-size:28px"><u>bitbra.in/slides/godotcon2023.pdf</u></center>

---
# Godot's Design Philosophy

> [...] new features from the core developers often focus on what will benefit the most users first.

<div style="margin-top:230px; font-size:20px;">
source:
https://docs.godotengine.org/en/stable/getting_started/introduction/godot_design_philosophy.html
</span>

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

<div style="margin-top:100px;font-size:25px;">
source:
https://github.com/coppolaemilio/dialogic/blob/main/addons/dialogic/plugin.cfg
</div>

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

<div style="margin-top:140px;font-size:20px;">
source:
https://github.com/utopia-rise/fmod-gdextension/blob/master/demo/addons/fmod/fmod.gdextension

</div>

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

![bg right:50%](assets/img/gdunit.png)

# Unit Testing

- `bitwes/Gut`
- `MikeSchulze/gdUnit4`
- `Spycemyster/GDMUT`
- `watplugin/wat`

---

Example unit test with `gdUnit4`:

```python
# GdUnit generated TestSuite
class_name PropertyTest extends GdUnitTestSuite


# TestSuite generated from
const __source = "res://addons/pandora/model/property.gd"


func test_string_property() -> void:
	var property = PandoraProperty.new("123", "property", "string")
	property.set_default_value("Hello World")
	var new_property = PandoraProperty.new("", "", "")
	new_property.load_data(property.save_data())
	assert_that(new_property).is_equal(property)
```
---

![bg width:90%](assets/img/github-actions.png)

---

# Integrations

![bg left:50%](assets/img/ethernet.jpg)

Connect any tool directly into Godot Engine.

---

![bg right:40%](assets/img/fmod-studio.jpg)

![width:300px](assets/img/fmod.png)

`utopia-rise/fmod-gdextension`

`alessandrofama/fmod-for-godot`

---


![bg left:40%](assets/img/balls.jpg)

![width:600px](assets/img/jolt-logo.svg)

Godot extension that integrates the Jolt physics engine.

`godot-jolt/godot-jolt`

<br/>

- works with `CharacterBody3D` and other familiar Godot nodes out of the box (drop-in replacement)


---

 # Other types of addons

- editor extensions
- language bindings
- templates
- shaders
- custom nodes
- themes

---
# Addon discovery

- Official: <u>godotengine.org/asset-library</u>
- Useful: <u>github.com/godotengine/awesome-godot</u>
- Goldmine: <u>github.com/search?q=godot%2Baddon</u>
- Supportive: <u>itch.io/search?q=godot%2Baddon</u>
- Bonus: <u>godotshaders.com</u>

---

# Is there an addon for that?

| S | M | L | XL |
|---|---|---|----|
| fix translation | add new language | add voicelines | dialogue system |
| change color of sword| update sword animation|add new weapon type| itemization system|
| fix sound timing| add new sound effect| dynamic sound playback | integrating FMOD |
| fix level collision | rework existing level | add new level | procedural level generation |
<!--
---

<center>

# Production Point Principle

### by 🖤 HeartBeast

<img class="avatar" src="assets/img/heartbeast.jpg">

<u>heartgamedev.substack.com/p/production-point</u>
</center>

---

![bg](assets/img/production-point.jpg)

<div style="font-size:22px;float:right; margin-top:-50px">source: <u>heartgamedev.substack.com/p/production-point</u></div>

---
# Content Pipeline

> Structured sequence of stages, tools, and methodologies used to conceptualize, design, develop, test, and deploy game content with consistency.

<b style="margin-left:50px;">&#9135; ChatGPT</b>
-->

---

# There is no silver bullet

- addons may become outdated
- addons may have bugs
- addons can have different design goals
- addons can break your game

![bg vertical left:50%](assets/img/brotato.png)

---

![bg](assets/img/siliconvalley.jpg)

<div style="color:white; margin-top:-60px">
<blockquote><p><i>You need to be twice as smart as the person who wrote the code in order to debug it.</i></p></blockquote>

<b style="margin-left:50px;">&#9135; Kernighan's Law</b>
</div>

---

# The DIY approach

- no external dependencies
- consistent standard & practices across all code
- any bug can be backtraced back to you (or Godot 😇)
- no docs to learn required

**BUT**

```
You need to know how to build it.
```

---

# When to probably use addons

- You do not want to build it yourself
- You have no time to build it yourself
- You want to build games, not technical systems
- You like to explore how others have solved a problem
- You want to get a headstart (e.g. gamejams) 

---

# Properties of a good addon

A **good** addon should be:

- useful
- well-documented
- well-presented
- tested
- **maintained** or **archived**
- compatible

---

# README.md

1. Recognizable Addon Logo
2. gifs and images showing what your addon does
3. how to install
4. compatibility matrix
5. how to contribute guide
6. wiki (e.g. via `docsify`)

---

# Interesting Proposals

- `#8114` Better discoverability of curated add-ons into editor
- `#7925` add-on manifests
- `#1205` New Add-On (sub-project) system
- `#831` Add support for global plugins/universal addons
- `#3367` Add ExtensionDevelopmentPlugin for in-editor native extension development


<span style="font-size:30px;">source: <u>github.com/godotengine/godot-proposals</u></span>

---

<center>

# Questions?

![width:350px](./assets/img/bitbrain-discord.svg)

### <u>youtube.com/@bitbraindev</u>

</center>