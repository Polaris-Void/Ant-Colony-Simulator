<div align="center">

![Platform](https://img.shields.io/badge/platform-Any%20Modern%20Browser-0078D6?logo=googlechrome&logoColor=white)
![Languages](https://img.shields.io/badge/languages-HTML%20%7C%20CSS%20%7C%20JavaScript-00569B?logo=javascript&logoColor=white)
![Dependencies](https://img.shields.io/badge/dependencies-Zero%20%7C%20Vanilla%20JS-22C55E?logo=none)
![License](https://img.shields.io/badge/license-Apache--2.0-FF6F61?logo=opensourceinitiative&logoColor=white)

English | [ÙØ§Ø±Ø³ÛŒ](README.FA.md)

</div>

# Ant Colony Simulator

A lightweight, **zero-dependency, single-file HTML5** simulation of a foraging ant colony â€” built entirely with **vanilla JavaScript** and the **HTML5 Canvas API**. Drop the file into any browser, and an entire ecosystem of scouts, workers, and carriers comes alive, laying pheromone trails between food sources and the nest.

No build tools, no npm, no frameworks â€” just one `.html` file.

---

## âœ¨ Features

- **ðŸœ True Swarm Intelligence:** Ants communicate exclusively through **pheromone trails** â€” home pheromone, food pheromone, and evaporation mechanics that mirror real colony foraging behavior.
- **ðŸ§¬ Three Ant Classes:** Scouts explore, workers transport, and carriers haul â€” each with distinct behaviors. Mix the colony composition with live sliders (0â€“100% per class).
- **âš™ï¸ Fully Tunable Simulation:** Adjust ant count (20â€“2500), movement speed, pheromone evaporation (0.85â€“0.9995), sensor range, and exploration factor â€” everything updates in real time.
- **ðŸ§  Behavior Modes:** Switch the colony between **Explorer**, **Balanced**, and **Exploiter** personality profiles.
- **ðŸ–Œï¸ Interactive Tools:** Paint food ðŸƒ, obstacles ðŸ§±, hazards ðŸ”¥, or erase with a adjustable brush size (1â€“10). Touch and mouse both supported.
- **ðŸ—ºï¸ Ready-Made Scenarios:** One-click terrains â€” Open Field ðŸŒ¾, Maze ðŸŒ€, Pillars ðŸ›, Corridor ðŸšª, Islands ðŸ, and Spiral ðŸŒª.
- **ðŸŽ¨ Themes & Appearance:** Multiple color palettes plus four ant rendering styles (Realistic, Simple, Dots, Streaks) and a pheromone-only view.
- **ðŸ”Š Ambient Audio:** Optional colony hum, chirps, event sounds, and milestone effects via the **Web Audio API** â€” no audio files needed.
- **ðŸŒ Bilingual UI:** Persian (RTL) and English â€” switch languages anytime; the choice is saved automatically.
- **ðŸ’¾ Persistent Settings:** All parameters and preferences are saved to `localStorage` â€” your colony survives a page refresh.
- **ðŸ“± Responsive & Mobile-Ready:** Adaptive layout, touch-friendly controls, and a collapsible control panel for phones and tablets.
- **ðŸ“Š Live Statistics:** Real-time colony stats (ant count, food collected, and more) right on the canvas.

---

## ðŸ“‹ System Requirements

- **Browser:** Any modern browser â€” Chrome, Edge, Firefox, or Safari (recent versions).
- **Dependencies:** None. The simulator is fully self-contained in a single `index.html` file.
- **Internet:** Not required. Everything runs locally on your machine.

---

## ðŸš€ How to Use

### 1. Run the Simulation Locally

1. Download or clone the repository.
2. Open `index.html` directly in your browser (double-click works), **or** serve it locally:

   ```powershell
   # Option A â€” simple Python server
   python -m http.server 8000

   # Option B â€” Node.js
   npx serve .
   ```

   Then open <http://localhost:8000> in your browser.

### 2. Control the Colony

- **Draw food** with the ðŸƒ brush by dragging on the canvas â€” ants will discover it and build trails.
- **Block paths** with the ðŸ§± wall brush, **burn** areas with ðŸ”¥ hazards, or **erase** with ðŸ§½.
- Use the **+ New Food** button to scatter random food sources instantly.
- Adjust every parameter live from the **âš™ Params**, **ðŸ§  Behavior**, **ðŸŽ¨ Themes**, **ðŸ—º Presets**, and **ðŸ”Š Audio** tabs.
- Press **ðŸ’¾ Save Settings** to freeze your colony's configuration for future sessions.
- Press **â™»ï¸ Reset Ecosystem** to start completely fresh.

---

## âŒ¨ï¸ Keyboard Shortcuts

| Key | Action |
| :--- | :--- |
| `Space` | Pause / Resume the simulation |
| `1` â€“ `4` | Switch between Food / Wall / Eraser / Hazard brushes |
| `[` / `]` | Decrease / Increase brush size |
| `F` | Toggle fullscreen |

---

## ðŸ§ª How It Works

The simulation is a real implementation of **Ant Colony Optimization (ACO)** principles:

1. **Scouts** wander randomly, drop food pheromone when they discover food, and lay home pheromone on the way back.
2. **Workers** follow the strongest pheromone gradient toward food and back to the nest, reinforcing successful trails.
3. **Carriers** focus on heavy transport between well-established routes.
4. Pheromones **evaporate** over time (rate adjustable), so stale routes fade and the colony adapts to changing terrain.
5. **Hazards** kill ants and erase pheromones in their radius â€” teach the colony to route around danger.

Because the whole engine is canvas-based and single-file, it's perfect for studying swarm behavior, teaching algorithms, or just watching tiny colonies find the shortest path â€” every run is different.

---

## ðŸ“ Project Structure

```
Ant-Colony-Simulator/
â”œâ”€â”€ Ant-Colony-Simulator.html  # The complete simulator (single file, zero dependencies)
â”œâ”€â”€ README.md                  # This file (English)
â”œâ”€â”€ README.FA.md               # Persian documentation
â”œâ”€â”€ LICENSE                    # Apache License 2.0
â””â”€â”€ Deploy-AntColonySim-SelfContained.ps1   # Self-contained script: docs + license + topics (no Git needed)
```

---

## â˜ï¸ Deploy to GitHub (Automated)

A complete **self-contained** PowerShell script is included â€” the two READMEs, the license and every configuration value are embedded *inside* the script itself. With **GitHub CLI** installed and authenticated (no local **Git** installation required), one run ensures the repository exists, adds the documentation, the license and the topics â€” all directly through the GitHub API:

```powershell
powershell -ExecutionPolicy Bypass -File .\Deploy-AntColonySim-SelfContained.ps1
```

Optional parameters:

| Parameter | Default | Description |
| :--- | :--- | :--- |
| `-RepoName` | `Ant-Colony-Simulator` | Name of the new GitHub repository |
| `-Description` | *(built-in)* | Repository description |
| `-Visibility` | `public` | `public` or `private` |

---

## ðŸ·ï¸ Repository Topics

Suggested GitHub topics for this project:

`ant-colony` Â· `simulation` Â· `javascript` Â· `html5` Â· `canvas` Â· `swarm-intelligence` Â· `algorithm` Â· `educational` Â· `interactive` Â· `single-file` Â· `zero-dependency`

---

## âš–ï¸ Absolute Legal Disclaimer, Waiver & Limitation of Liability

This project is licensed under the **Apache License, Version 2.0**. This disclaimer expressly supplements, expands, and reinforces **Section 7 (Disclaimer of Warranty)** and **Section 8 (Limitation of Liability)** of the Apache License 2.0, and shall control to the maximum extent permitted by applicable law.

**FOR EDUCATIONAL, RESEARCH, AND INFORMATIONAL PURPOSES ONLY. NO COMMERCIAL WARRANTY OR LIABILITY IS ASSUMED.**

### 1. Complete Disclaimer of All Warranties
To the maximum extent permitted by applicable law, the Software (including all code, documentation, data, and related materials) is provided strictly on an **"AS IS"** and **"AS AVAILABLE"** basis, without any warranties or conditions of any kind, whether express, implied, statutory, customary, or otherwise. This includes, without limitation, any warranties of merchantability, fitness for a particular purpose, non-infringement, title, security, accuracy, completeness, uninterrupted or error-free operation, or freedom from viruses or other harmful components. The author(s), copyright holder(s), maintainer(s), and contributor(s) expressly disclaim all such warranties.

### 2. Absolute Limitation of Liability
Under no circumstances and under no legal theory (whether in contract, tort â€” including negligence, gross negligence, and willful misconduct â€” strict liability, product liability, or otherwise) shall the author(s), contributor(s), or copyright holder(s) be liable for any damages whatsoever, including but not limited to direct, indirect, incidental, special, consequential, exemplary, punitive, or any other damages (including loss of data, profits, revenue, business interruption, system failure, hardware damage, security breaches, personal injury, or any other loss), arising out of or related to the use, inability to use, modification, distribution, or reliance upon the Software, even if advised of the possibility of such damages and even if any remedy fails of its essential purpose.

### 3. Assumption of All Risk & User Responsibility
Any use, cloning, modification, deployment, distribution, or reliance upon this Software is undertaken entirely at the user's sole risk and discretion. The user is exclusively and solely responsible for:

- Ensuring full compliance with all applicable local, national, and international laws, regulations, export controls, and third-party terms;
- Evaluating the suitability, security, and legality of the Software for any purpose;
- Any consequences arising from its use or misuse.

Nothing in this repository constitutes legal, financial, cybersecurity, medical, architectural, or any other form of professional advice.

### 4. Broad Indemnification
By accessing, downloading, cloning, forking, viewing, compiling, distributing, or using any part of this repository, you irrevocably agree to indemnify, defend, and hold harmless the author(s), contributor(s), and copyright holder(s) from and against any and all claims, demands, actions, proceedings, liabilities, damages, losses, costs, and expenses (including reasonable attorney's fees and legal costs) arising out of or related to your access, use, misuse, modification, distribution, or violation of this disclaimer or any applicable law.

### 5. Severability & Maximum Enforceability
If any provision of this disclaimer is held to be unenforceable or invalid under applicable law, such provision shall be modified to the minimum extent necessary to make it enforceable, or if modification is not possible, severed. The remaining provisions shall continue in full force and effect. This disclaimer shall be interpreted to provide the maximum protection permitted by law.

### 6. No Waiver of Non-Waivable Rights
Nothing in this disclaimer is intended to exclude or limit any liability that cannot be excluded or limited under applicable mandatory law (including liability for death or personal injury caused by negligence in jurisdictions where such exclusion is prohibited). In such cases, liability is limited to the maximum extent permitted by law.

---

*Made with ðŸœ by [Polaris-Void](https://github.com/Polaris-Void)*