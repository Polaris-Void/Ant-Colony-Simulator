![Platform](https://img.shields.io/badge/platform-Web%20Browser-00F2FE?logo=html5&logoColor=white)
![License](https://img.shields.io/badge/license-Apache--2.0-blue)

English | [فارسی](README.FA.md)

# Interactive Ant Colony Simulator & Pheromone Sandbox

A lightweight, single-file HTML simulator where thousands of ants forage for food, lay pheromone trails, and find their way around obstacles that you draw yourself.

Zero installation, zero dependencies — just open the file in your browser.

---

## ✨ Features

- **🐜 Pheromone-Based Foraging:** Ants leave "return" trails while searching and "food" trails while carrying food, and follow trails using three forward-facing sensors.
- **🧭 Three Ant Types:** Scouts, Workers, and Carriers, each with its own speed, trail strength, and exploration tendency. The mix is adjustable.
- **🖌️ Interactive Sandbox:** Tap to place food, or draw walls and hazard zones with an adjustable brush (size 1–10). An eraser removes obstacles and trails.
- **🗺️ 6 Ready-Made Scenarios:** Open Field, Maze, Pillars, Corridor, Islands, and Spiral.
- **🌍 8 Terrains & 12 Color Themes:** Sand, Forest, Stone, Grass, Moon, Snow, Savanna, and Obsidian, combined with palettes like Neon Night, Cyberpunk, Ocean, Matrix, and more.
- **🧠 Behavior Modes:** Switch the colony between Explorer, Balanced, and Exploiter, and run time from 0.5× up to 4×.
- **🎨 4 Ant Display Styles:** Realistic (animated walking sprites), Simple, Dots, and Streaks — plus a "trails only" view.
- **🔊 Synthesized Audio:** Ambient drone, chirps, event sounds, and milestone chimes generated with the Web Audio API. No audio files are used, and sound is off until you enable it.
- **🌐 Bilingual Interface:** Persian (RTL) and English (LTR), switchable at any time.
- **📱 Responsive Design:** A bottom sheet on phones and tablets, and a side panel on desktop. Fullscreen is supported.
- **⚡ Zero Dependencies:** One HTML file with no libraries, no build step, and no network requests.

---

## 🖼️ Preview

> **Placeholder:** Add screenshots or a short GIF here.

| Open Field | Maze |
| :---: | :---: |
| `docs/screenshot-open.png` | `docs/screenshot-maze.png` |

> **Placeholder (optional):** Live demo link — `https://<your-username>.github.io/<repo-name>/`

---

## 💻 System Requirements

- **Browser:** A modern desktop or mobile browser with HTML5 Canvas, Pointer Events, and JavaScript enabled. *(Assumption: current versions of Chrome, Edge, Firefox, and Safari; specific versions were not tested for this README.)*
- **Audio (optional):** A browser that supports the Web Audio API.
- **Permissions:** None. Nothing is installed and no network access is needed.

---

## 🚀 How to Use

1. Download this repository and open **`Ant-Colony-Simulator.html`** in your browser.
2. Pick a tool from the **🖌 Tools** tab:
   - **🍃 Food** — tap anywhere to drop a food pile.
   - **🧱 Wall** — drag to draw obstacles.
   - **🔥 Hazard** — drag to draw danger zones that ants will not enter.
   - **🧽 Eraser** — drag to remove walls, hazards, and pheromone trails.
3. Watch the ants discover food, lay trails, and settle into efficient paths.
4. Open the **🗺 Presets** tab to load a ready-made map, or **⚙ Params** to tune the colony.
5. Tap **💾 Save Settings** to keep your theme, terrain, language, and parameters for next time.

**Opening the control panel:**
- **Phone / tablet:** Tap the round button (top corner) or drag the handle at the bottom of the screen.
- **Desktop (≥ 768 px wide):** The panel is shown on the side. Use ✕ to collapse it and click the mini bar to reopen.

### 🎮 Keyboard Shortcuts (Desktop)

| Key | Action |
| :--- | :--- |
| `Space` | Pause / Resume |
| `1` – `4` | Food / Wall / Eraser / Hazard |
| `[` `]` (or `-` `+`) | Decrease / Increase brush size |
| `F` | Toggle fullscreen |
| `M` | Toggle sound |

---

## ⚙️ Configuration

All settings are available in the in-app panel — no files need to be edited.

| Tab | What you can change |
| :--- | :--- |
| 🖌 **Tools** | Brush type and size, spawn new food, pause, clear pheromones, clear obstacles |
| 🌍 **Terrain** | Ground texture and terrain brightness |
| ⚙ **Params** | Ant count, movement speed, pheromone persistence, sensor distance, exploration factor, ant type mix |
| 🧠 **Behavior** | Colony mode, time scale, ant appearance, "trails only" view, particles |
| 🎨 **Themes** | 12 color palettes (affects trails, ants, and UI accents) |
| 🗺 **Presets** | 6 scenarios, plus saving settings |
| 🔊 **Audio** | Volume, ambient sound, event sounds, milestone sounds |

| Parameter | Range | Default |
| :--- | :--- | :--- |
| Ant count | 20 – 2500 | 1200 |
| Movement speed | 0.1 – 25 | 4.0 |
| Pheromone persistence | 0.85 – 0.9995 | 0.99 |
| Sensor distance | 5 – 100 px | 25 |
| Exploration factor | 0.01 – 2 | 0.22 |
| Ant mix (Scout / Worker / Carrier) | 0 – 100 each (relative weights) | 30 / 50 / 20 |
| Brush size | 1 – 10 | 1 |
| Time scale | 0.5× / 1× / 2× / 4× | 1× |

---

## 🧠 How It Works

- **Two pheromone fields:** Ants without food deposit *return* pheromone; ants carrying food deposit *food* pheromone. Searching ants follow the food field, loaded ants follow the return field.
- **Sensing & steering:** Each ant samples the field with three sensors (front, left, right) and turns toward the strongest signal, with some random wandering. Walls and hazards are impassable and read as "no signal".
- **Ant types:** Scouts are fast and explore widely, Workers are balanced, and Carriers are slow but lay the strongest trails.
- **Fixed 60 Hz simulation step:** Behavior is consistent on different screen refresh rates. Time scale only changes how many steps run per frame.
- **Performance:** Ant data lives in typed arrays, the pheromone grid is processed in chunks (inactive areas are skipped), and ant sprites are pre-rendered. Above 2,200 ants, *Realistic* and *Simple* styles fall back to dots.
- **Procedural everything:** Terrain, walls, ants, and all audio are generated at runtime — there are no image or audio assets.

---

## ❓ FAQ

**Do I need to install anything or run a server?**
No. The project is a single HTML file that runs locally in your browser.

**Why is there no sound at first?**
Sound is off by default. Tap the 🔇 button (or press `M`) to enable it. Browsers only allow audio after a user interaction.

**Are my drawn walls saved?**
No. *Save Settings* stores your theme, terrain, language, and parameters. Maps, walls, pheromone trails, and terrain brightness are not saved.

**Why did my walls and trails disappear when I resized the window or toggled fullscreen?**
The simulation grid is rebuilt when the screen size changes. Food piles and ants are kept, but drawn obstacles and pheromone trails are cleared.

**What do hazards do?**
Hazards are impassable like walls, and ants steer around them. They are drawn with a pulsing red glow.

**Is there a Persian interface?**
Yes. Persian (RTL) is the default. Use the 🌐 button to switch between Persian and English.

---

## 🤝 Contributing

Issues and pull requests are welcome. Please keep the project **single-file and dependency-free**, and keep the Persian and English UI strings in sync when adding text. For larger changes, open an issue first.

---

## 📜 License

This project is licensed under the **Apache License, Version 2.0**.
---

## ⚖️ Absolute Legal Disclaimer, Waiver & Limitation of Liability

This project is licensed under the **Apache License, Version 2.0**. This disclaimer expressly supplements, expands, and reinforces **Section 7 (Disclaimer of Warranty)** and **Section 8 (Limitation of Liability)** of the Apache License 2.0, and shall control to the maximum extent permitted by applicable law.

**FOR EDUCATIONAL, RESEARCH, AND INFORMATIONAL PURPOSES ONLY. NO COMMERCIAL WARRANTY OR LIABILITY IS ASSUMED.**

### 1. Complete Disclaimer of All Warranties

To the maximum extent permitted by applicable law, the Software (including all code, documentation, data, and related materials) is provided strictly on an **"AS IS"** and **"AS AVAILABLE"** basis, without any warranties or conditions of any kind, whether express, implied, statutory, customary, or otherwise. This includes, without limitation, any warranties of merchantability, fitness for a particular purpose, non-infringement, title, security, accuracy, completeness, uninterrupted or error-free operation, or freedom from viruses or other harmful components. The author(s), copyright holder(s), maintainer(s), and contributor(s) expressly disclaim all such warranties.

### 2. Absolute Limitation of Liability

Under no circumstances and under no legal theory (whether in contract, tort — including negligence, gross negligence, and willful misconduct — strict liability, product liability, or otherwise) shall the author(s), maintainer(s), contributor(s), or copyright holder(s) be liable for any damages whatsoever, including but not limited to direct, indirect, incidental, special, consequential, exemplary, punitive, or any other damages (including loss of data, profits, revenue, business interruption, system failure, hardware damage, security breaches, personal injury, or any other loss), arising out of or related to the use, inability to use, modification, distribution, or reliance upon the Software, even if advised of the possibility of such damages and even if any remedy fails of its essential purpose.

### 3. Assumption of All Risk & User Responsibility

Any use, cloning, modification, deployment, distribution, or reliance upon this Software is undertaken entirely at the user’s sole risk and discretion. The user is exclusively and solely responsible for:

- Ensuring full compliance with all applicable local, national, and international laws, regulations, export controls, and third-party terms;
- Evaluating the suitability, security, and legality of the Software for any purpose;
- Any consequences arising from its use or misuse.

Nothing in this repository constitutes legal, financial, cybersecurity, medical, architectural, or any other form of professional advice.

### 4. Broad Indemnification

By accessing, downloading, cloning, forking, viewing, compiling, distributing, or using any part of this repository, you irrevocably agree to indemnify, defend, and hold harmless the author(s), contributor(s), and copyright holder(s) from and against any and all claims, demands, actions, proceedings, liabilities, damages, losses, costs, and expenses (including reasonable attorneys’ fees and legal costs) arising out of or related to your access, use, misuse, modification, distribution, or violation of this disclaimer or any applicable law.

### 5. Severability & Maximum Enforceability

If any provision of this disclaimer is held to be unenforceable or invalid under applicable law, such provision shall be modified to the minimum extent necessary to make it enforceable, or if modification is not possible, severed. The remaining provisions shall continue in full force and effect. This disclaimer shall be interpreted to provide the maximum protection permitted by law.

### 6. No Waiver of Non-Waivable Rights

Nothing in this disclaimer is intended to exclude or limit any liability that cannot be excluded or limited under applicable mandatory law (including liability for death or personal injury caused by negligence in jurisdictions where such exclusion is prohibited). In such cases, liability is limited to the maximum extent permitted by law.
