# 🤖 AI-Powered 3D Rubik's Cube Solver

### ✨ Features

* **Interactive 3D Cube:** A fully interactive 3D model built with **Three.js**. Drag to rotate, zoom, and inspect the cube from any angle.
* **Real-Time Solving:** Implements a genuine Layer-by-Layer (LBL) algorithm to solve the cube. Watch the solution animate step-by-step.
* **Random Scramble:** Generate a standard, random 20-move scramble to test the solver.
* **🤖 AI-Powered Pattern Suggestions:** Click "Suggest Pattern" to call the **Gemini API** and receive a unique, named scramble pattern (e.g., "The Serpent's Twist," "Galactic Gambit").
* **🤖 AI-Powered Explanations:** After a solution is found, click "Explain Solution" to send the algorithm to the Gemini API. It returns a high-level, easy-to-understand breakdown of the solving phases (White Cross, F2L, OLL, PLL).
* **Responsive Design:** A clean, modern UI that works seamlessly on both desktop and mobile devices.

### 🛠️ Tech Stack

This project is built entirely with frontend technologies, running in the browser.

* **3D Rendering:**
    * **Three.js (r128):** The core library for creating and managing the 3D scene, camera, lighting, and cube geometries.
    * **WebGL:** The underlying graphics API used by Three.js to render the cube on the HTML `<canvas>`.
* **User Interface:**
    * **HTML5:** Provides the structure for the application.
    * **Tailwind CSS:** A utility-first CSS framework for rapidly building the modern, responsive UI.
* **Core Logic & Interactivity:**
    * **JavaScript (ES6+):** Handles all application logic, state management, user interactions, and animations.
* **AI Integration:**
    * **Google Gemini API:** Used for the "Suggest Pattern" and "Explain Solution" features. The application makes direct `fetch` calls to the Gemini REST API.


---

### 📜 License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
