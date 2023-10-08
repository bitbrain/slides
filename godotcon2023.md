---
theme: dash
paginate: true
marp: true
---

![bg left:40% 60%](assets/godot.png)

# **Super-charging content production with Godot addons**

Building a pipeline to predictable produce game content. 

---

# The Dream Game Problem

Who here has failed at least one dream game project?

---

# The Scope Creep Monster

AAAAARGH!!!

---

# Project Management Triangle

- quality is a trade off between time, cost and scope!
- the larger the scope, the more time it takes
- the more time something takes, the more it costs
- with a fixed budget, scope needs to be fixated to avoid feature creep

---

# A typical game setup

- show diagram of a game's setup such as graphics, audio, level design, world building, story telling, AI, game mechanics, systems
- ask the question: how could you reduce or increase scope in each of these?

---
# The Godot Onion

- show the onion: Godot core in the center, then various layers that show extensions/addons + custom game code

---

# Should I use an addon for that?

- there are plenty of addons available that aim to solve all sorts of problems
- how do I know what addon is best for the job?
- should I even use an addon?
- maybe writing it yourself is better after all?

---

# "Just use an addon"

- is the problem complex enough that it would take up a lot of time and effort for you to solve it?
- is the addon well maintained?
- is an addon even available?

---

# "Just build it yourself"

- are you currently "reinventing" the wheel like writing another dialogue manager with complex branching logic?
- is the problem you are trying to solve unique to your game?

--- 

# Pitfalls of using an addon

- **Versioning & Compatibility** - does the addon define how it aims to stay compatible with future Godot versions?
- **Documentation & Community** - are there any docs on how to use the addon? Are there people to ask questions about its usage?
- **Quality Assurance** - how are features & bugfixes tested? Are there any sort of test automation?

---

# Tipps for using an addon

- YAGNI ("You Aint Gonna Need It")
- always consider if writing it yourself makes sense, given your available time & budget.
- using addons can be a great way to benefit from a community without having to build it yourself (tradeoff: customization vs. time saving)
- validate an addons pitfalls and create a small prototype if necessary to test it

---

# Tipps for creating an addon

- research if somebody solved the issue before
- keep the addon generic and independent of specific game requirements
- do not assume a particular game setup. Giving addon users freedom empowers them to do awesome things!

---
# Example: FMOD GDExtension

- allows for integrating FMOD Studio into Godot
- FMOD has been used by games like Celeste
- allows for better collaboration with sound engineers
---

# Example: Pandora

- RPG Data Management (General Purpose)
- Alternative to Godot resources (but can be used in combination with Godot resources)
- inspired by GridlessDB

---

# Example: Beehave

- Behaviour Tree AI
- 100% node based
- Composition over Inheritance
- Dedicated Debugger
---
# Thank you!

I am using all these addons in my untitled RPG called cave.

Follow me on youtube.com/@bitbraindev for devlogs and Godot tutorials!

---