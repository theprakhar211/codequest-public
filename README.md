<div align="center">

<h1>🎮 CodeQuest — Learn to Code Through Adventure</h1>

<p><strong>A 2D RPG where Python is your sword and logic is your shield.</strong></p>

[![Portfolio](https://img.shields.io/badge/Portfolio-prakhar--sharma.vercel.app-64748b?style=flat-square&logo=vercel&logoColor=white)](https://prakhar-sharma.vercel.app)

![Godot](https://img.shields.io/badge/Godot_4-478CBF?style=flat-square&logo=godotengine&logoColor=white)
![GDScript](https://img.shields.io/badge/GDScript-478CBF?style=flat-square&logo=godotengine&logoColor=white)
![Status](https://img.shields.io/badge/Status-In_Development-f59e0b?style=flat-square)

> 🔒 **This repository is public for visibility. Source code is kept private to protect ongoing development.**
> To request access, email [theprakhar211@gmail.com](mailto:theprakhar211@gmail.com?subject=Code%20Request%20-%20CodeQuest)

</div>

---

## 📌 Overview

CodeQuest is a 2D RPG adventure game built in the Godot Engine that transforms programming education into an interactive gameplay experience. Instead of tutorials and text boxes, players explore handcrafted maps, interact with NPCs, complete quests, and use **real Python code** through an in-game console to solve problems and unlock new areas.

The core idea: coding isn't a subject — it's a mechanic. Every programming concept is woven directly into the gameplay loop rather than bolted on as an exercise.

---

## 🎯 Concept

Traditional coding education is passive — read, watch, repeat. CodeQuest makes it active:

- 🗺️ **Explore** a handcrafted game world with interconnected maps and areas
- 🧙 **Talk** to NPCs who give quests requiring code to complete
- 💻 **Write real Python** in the in-game console to interact with the world
- 🔓 **Unlock** new areas, abilities, and story beats by solving logic challenges
- 📖 **Learn** programming concepts naturally through context, not memorisation

---

## ✨ Features

### 🕹️ Core Gameplay Systems
- **Player movement & exploration** — smooth 2D movement across handcrafted tile maps
- **Camera system** — follows the player with smooth lerp, respects map boundaries
- **NPC dialogue system** — branching conversations that trigger quests and story events
- **Quest system** — tracks active, completed, and available quests with objectives

### 💻 In-Game Coding Console
The centrepiece of the game. An integrated console where players write actual Python code to interact with game objects and solve puzzles.

- Input validation runs locally before any execution
- Logic engine evaluates whether the player's solution is correct for the given challenge
- Contextual feedback — tells you *why* a solution is wrong, not just that it failed
- Console persists across scenes so players can reference previous attempts

### 🗺️ World Design
- Multiple handcrafted maps connected by transitions
- Each area introduces a new programming concept through its environment and challenges
- Hidden areas unlockable only through specific code solutions

### 🎨 UI/UX
- Custom UI built entirely in Godot's Control nodes
- In-game HUD showing quest objectives, player stats, and console toggle
- Dialogue boxes with typewriter effect and NPC portraits
- Inventory and quest log screens

---

## 🏗️ Architecture & Design Decisions

### Modular Scene Structure
Every system is built as an independent Godot scene — player, NPC, dialogue, console, map transitions. This makes adding new quests and areas straightforward without touching unrelated systems.

### Custom Logic Engine
The evaluation system doesn't just check if code runs — it checks if it solves the problem correctly. Each challenge has an expected output or world state defined in a data file. The logic engine compares the result of the player's code against the expected outcome and generates targeted feedback.

### Data-Driven Quest Design
Quests and challenges are defined in external data files rather than hardcoded into scenes. This means new content can be added without modifying core game logic — the engine reads the quest data and sets up the challenge automatically.

### GDScript + Python Bridge
The game is built in GDScript (Godot's native language) but the player writes Python. A lightweight bridge layer handles passing player input to the evaluation system, running it in a sandboxed context, and returning the result to the game world.

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Engine | Godot 4 |
| Language | GDScript |
| Player code | Python (sandboxed) |
| Maps | Godot TileMap system |
| UI | Godot Control nodes |
| Data | JSON / GDScript resources |

---

## 📁 Project Structure

```
CodeQuest/
├── scenes/
│   ├── player/          # Player character, movement, stats
│   ├── npcs/            # NPC base class + individual characters
│   ├── maps/            # Individual map scenes + TileMap layers
│   ├── ui/              # HUD, dialogue box, quest log, console
│   └── systems/         # Game manager, quest tracker, event bus
├── scripts/
│   ├── player.gd        # Movement, interaction, camera follow
│   ├── dialogue.gd      # Branching dialogue engine
│   ├── quest_manager.gd # Quest state, objectives, completion
│   ├── console.gd       # In-game coding console
│   └── logic_engine.gd  # Solution evaluation, feedback generation
├── data/
│   ├── quests/          # Quest definitions (JSON)
│   └── challenges/      # Coding challenge specs + expected outputs
├── assets/
│   ├── sprites/
│   ├── tilesets/
│   └── fonts/
└── README.md
```

---

## 🗺️ Roadmap

- [x] Player movement & camera system
- [x] NPC dialogue system
- [x] Map design & transitions
- [x] In-game coding console
- [x] Logic engine — basic solution evaluation
- [ ] Quest system — full objective tracking
- [ ] Multiple maps with concept progression
- [ ] Web export for browser play
- [ ] Sound design & music

---

## ⚠️ Known Limitations / In Progress

- **Web export** — currently desktop only. Browser port via Godot's HTML5 export is planned
- **Python sandboxing** — the bridge between GDScript and Python evaluation is still being hardened
- **Content** — world and quest content actively being expanded

---

## 👤 Author

**Prakhar Sharma**
[Portfolio](https://prakhar-sharma.vercel.app) · [LinkedIn](https://www.linkedin.com/in/prakhar-sharma-21112004-) · [Email](mailto:theprakhar211@gmail.com)

> 💌 Interested in the code or want to collaborate? [Request access](mailto:theprakhar211@gmail.com?subject=Code%20Request%20-%20CodeQuest)

---

## 📄 License

MIT
