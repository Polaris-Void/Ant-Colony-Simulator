English | [فارسی](README.FA.md)

# Ant Colony Simulator

A pure, zero-dependency, single-file HTML5 simulation of an ant colony. Ants deposit and follow pheromone trails, collect food, and interact with walls and hazards in real time. Fully bilingual (English / Persian), mobile-friendly, and designed to run offline with no build step or external libraries.

---

## ✨ Features

* **🐜 Realistic Ant Behavior** — Scouts, workers, and carriers with different speed, pheromone strength, and exploration tendencies.
* **🧪 Dual Pheromone System** — Separate home and food pheromone fields with evaporation, diffusion, and visual trails.
* **🖌 Interactive Tools** — Draw food sources, walls, hazards, or erase with adjustable brush size. Continuous line drawing supported.
* **🌍 Multiple Terrains** — Sand, Forest, Stone, Grass, Moon, Snow, Savanna, and Obsidian with matching wall textures.
* **🎨 12 Color Themes** — Neon Night, Cyberpunk, Ocean, Sunset, Matrix, Candy, Amber, Fire, Ice, Vaporwave, Forest, and Monochrome.
* **🗺 Ready-made Presets** — Open Field, Maze, Pillars, Corridor, Islands, and Spiral.
* **⚙️ Deep Parameters** — Ant count (up to 2500), speed, evaporation rate, sensor distance, wander factor, and ant-type mix.
* **🧠 Behavior Modes** — Explorer, Balanced, and Exploiter presets that automatically adjust exploration vs. exploitation.
* **📱 Fully Responsive** — Optimized for both mobile (bottom sheet controls) and desktop (side panel).
* **🔊 Optional Audio** — Ambient drone + event sounds and milestone chimes (Web Audio API).
* **🌐 Bilingual UI** — Instant language switch between Persian (RTL) and English (LTR). Settings are saved in localStorage.
* **💾 Persistent Settings** — Theme, terrain, parameters, and language are remembered across sessions.

---

## 🚀 How to Use

### Online (GitHub Pages)

Just open the live demo (once published):

`https://polaris-void.github.io/Ant-Colony-Simulator/`

### Offline / Local

1. Download or clone this repository.
2. Open `index.html` in any modern browser (Chrome, Firefox, Edge, Safari).
3. No installation, no server, no dependencies required.

### Controls (Desktop)

| Key / Action       | Effect                          |
|--------------------|---------------------------------|
| Space              | Pause / Resume                  |
| 1 – 4              | Switch brush (Food / Wall / Erase / Hazard) |
| [  or  -           | Decrease brush size             |
| ]  or  =           | Increase brush size             |
| F                  | Toggle fullscreen               |
| M                  | Toggle sound                    |

On mobile, use the floating action button and bottom panel.

---

## 📋 System Requirements

* Any modern browser with HTML5 Canvas and ES6 support (last 4–5 years).
* Works offline. No network access is required after the first load.
* Recommended: hardware acceleration enabled for smooth performance with 1500+ ants.

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

* Ensuring full compliance with all applicable local, national, and international laws, regulations, export controls, and third-party terms;
* Evaluating the suitability, security, and legality of the Software for any purpose;
* Any consequences arising from its use or misuse.

Nothing in this repository constitutes legal, financial, cybersecurity, medical, architectural, or any other form of professional advice.

### 4. Broad Indemnification

By accessing, downloading, cloning, forking, viewing, compiling, distributing, or using any part of this repository, you irrevocably agree to indemnify, defend, and hold harmless the author(s), contributor(s), and copyright holder(s) from and against any and all claims, demands, actions, proceedings, liabilities, damages, losses, costs, and expenses (including reasonable attorneys’ fees and legal costs) arising out of or related to your access, use, misuse, modification, distribution, or violation of this disclaimer or any applicable law.

### 5. Severability & Maximum Enforceability

If any provision of this disclaimer is held to be unenforceable or invalid under applicable law, such provision shall be modified to the minimum extent necessary to make it enforceable, or if modification is not possible, severed. The remaining provisions shall continue in full force and effect. This disclaimer shall be interpreted to provide the maximum protection permitted by law.

### 6. No Waiver of Non-Waivable Rights

Nothing in this disclaimer is intended to exclude or limit any liability that cannot be excluded or limited under applicable mandatory law (including liability for death or personal injury caused by negligence in jurisdictions where such exclusion is prohibited). In such cases, liability is limited to the maximum extent permitted by law.