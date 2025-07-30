# 🤖 AI-Powered 3D Rubik's Cube Solver

![Rubik's Cube Solver Demo](https://storage.googleapis.com/gemini-prod/images/c29c8e8d-876e-4e9b-8919-866465492d05)

An interactive, browser-based 3D Rubik's Cube solver that not only finds the solution to any valid scramble but also uses the **Google Gemini API** to provide creative scramble patterns and explain the solution steps in plain English.

---

### ✨ Features

* **Interactive 3D Cube:** A fully interactive 3D model built with **Three.js**. Drag to rotate, zoom, and inspect the cube from any angle.
* **Real-Time Solving:** Implements a genuine Layer-by-Layer (LBL) algorithm to solve the cube. Watch the solution animate step-by-step.
* **Random Scramble:** Generate a standard, random 20-move scramble to test the solver.
* **🤖 AI-Powered Pattern Suggestions:** Click "Suggest Pattern" to call the **Gemini API** and receive a unique, named scramble pattern (e.g., "The Serpent's Twist," "Galactic Gambit").
* **🤖 AI-Powered Explanations:** After a solution is found, click "Explain Solution" to send the algorithm to the Gemini API. It returns a high-level, easy-to-understand breakdown of the solving phases (White Cross, F2L, OLL, PLL).
* **Responsive Design:** A clean, modern UI that works seamlessly on both desktop and mobile devices.

---

### 🚀 Live Demo

**[Click here to try the solver live!](https://your-live-demo-link-here.com)** *(Note: This is a placeholder link. You would replace this with the actual URL where you host the application.)*

---

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

### ⚙️ How It Works

1.  **3D Visualization:** The cube is not a single object but a collection of 26 individual "cubies" arranged in a 3x3x3 grid. When a move is performed (e.g., `R`), the application identifies all cubies on the right face, attaches them to a central `pivot` object, rotates the pivot 90 degrees, and then reattaches the cubies to the main scene in their new positions.
2.  **Solving Algorithm:** The application uses a built-in, programmatic Layer-by-Layer (LBL) solver. When "Solve" is clicked, it analyzes the cube's abstract state and generates a valid sequence of moves to solve it phase by phase.
3.  **Gemini API Integration:**
    * **Pattern Suggestion:** A carefully crafted prompt is sent to the Gemini API asking for a creative name and a valid 20-move scramble, with instructions to return the data in a specific JSON format.
    * **Solution Explanation:** The generated solution string is sent to the Gemini API. The prompt asks the AI to act as a helpful tutor and explain the sequence by breaking it down into logical solving phases.

---

### 🏁 Getting Started

This project is a single, self-contained HTML file and requires no build process or installation.

1.  **Clone the repository (or download the HTML file):**
    ```bash
    git clone [https://github.com/your-username/rubiks-solver.git](https://github.com/your-username/rubiks-solver.git)
    ```
2.  **Navigate to the directory:**
    ```bash
    cd rubiks-solver
    ```
3.  **Open the `.html` file in your web browser.** That's it!

**Note:** To enable the Gemini API features, you would need to get a free API key from [Google AI Studio](https://aistudio.google.com/) and paste it into the `API_KEY` constant in the `<script>` tag.

---

### 📜 License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
