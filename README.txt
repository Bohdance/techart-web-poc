# Interactive HTML5 Canvas Asset: TechArt PoC

![Tech Stack](https://img.shields.io/badge/Tech-HTML5_Canvas-orange)
![Tech Stack](https://img.shields.io/badge/Tech-JavaScript-yellow)
![Tech Stack](https://img.shields.io/badge/Tech-Adobe_Animate-red)

A technical proof-of-concept demonstrating the integration of optimized 2D web animations with external JavaScript logic and JSON-driven state data. Built specifically to showcase a lightweight, engine-agnostic pipeline for web-based games (iGaming / Web GameDev).

> **Note:** This project focuses on the intersection of art and engineering, prioritizing draw-call optimization, state decoupling, and pipeline efficiency over complex frontend frameworks.

* **JavaScript State Machine:** Implemented a lightweight FSM with distinct animation states (`Idle`, `Fail`, `Success`). Animation playback is cleanly decoupled from the core logic via Frame Labels.
* **Data-Driven Integration:** Transition rules and variables (e.g., carbide resource levels) are fetched from an external `config.json` using the Fetch API, mimicking real-time backend/server responses.
* **Custom DOM Debug UI:** Engineered an in-browser overlay panel using vanilla DOM manipulation. This allows QA or Game Designers to mutate state variables on the fly and test animation triggers without page reloads.
* **VFX Performance Optimization:** Audited and refactored vector-based particle effects to avoid `Cache as Bitmap` rendering overhead, ensuring smooth frame rates without unnecessary rasterization.

## 🚀 How to Run Locally

Because this project uses the `fetch()` API to read the `config.json` file, it must be run on a local web server to avoid browser CORS (Cross-Origin Resource Sharing) restrictions. Do not just double-click the HTML file.

**Using VS Code:**
1. Install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension.
2. Open this folder in VS Code.
3. Right-click `index.html` and select **"Open with Live Server"**.

**Using Python:**
1. Open your terminal in this directory.
2. Run the built-in server: `python3 -m http.server 8000`
3. Open `http://localhost:8000` in your web browser.

## 📁 Repository Structure

* `index.html` — The main entry point and canvas container.
* `Carbide_Lamp_Main.js` (Generated) — The core logic file containing the compiled Animate library, State Machine, and custom UI generation code.
* `config.json` — External configuration file for testing data-driven logic.
* `/images` — Sprite sheets and texture atlases exported from the pipeline.