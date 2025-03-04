# SEPM
Clock UI Game

# Clock Game UI Module
This is the **Clock UI Module** for the **UU-GAME** project. It provides a graphical user interface for the **Clock Game**, handling user interactions, level selection, and communication with the **Clock Logic Module** and **Backend Module**.

---

## 📁 Project Structure
```
clock_game/
├── assets/                # Stores images and game progress data
│   ├── UU-logo            # Background logo for the Clock Game UI
│   ├── progress.json      # Stores game progress and leaderboard data
│
├── __pycache__/           # Auto-generated Python cache files
│
├── backend_connector.py   # Manages data storage & leaderboard retrieval
├── game_logic_connector.py # Handles game logic (questions, answers, hints)
├── main.py                # Entry point for the Clock Game
├── run_game.py            # Manually runs the Clock Game without the Main Menu
├── ui.py                  # Manages the Clock Game UI
├── README.md              # Project documentation
```

---

## 🚀 How to Run the Game
### 1️⃣ Run the Game From the Main Menu
If the **Main Menu Module** is managing the game, it will call:
```python
from main import start_clock_game
start_clock_game()
```

### 2️⃣ Run the Game Manually
If you want to test the game **without the Main Menu**, run:
```sh
python run_game.py
```

---

## 🛠 Dependencies
Ensure you have **Python 3.x** installed and the required libraries:
```sh
pip install pillow tkinter
```

---

## 🔹 Module Descriptions
### 1️⃣ `ui.py` (Clock Game UI)
- Displays the main menu, level selection, leaderboard, and reset game button.
- Handles user interactions and communicates with **Game Logic** and **Backend** modules.
- Supports **returning to the Main Menu**.

### 2️⃣ `backend_connector.py` (Backend Integration)
- Manages **game progress (progress.json)** and **leaderboard retrieval**.
- Stores game state in `assets/progress.json`.
- Functions:
  - `load_progress()`
  - `save_progress()`
  - `reset_progress()`
  - `get_leaderboard()`

### 3️⃣ `game_logic_connector.py` (Game Logic)
- Handles **question generation, validation, and hints**.
- Manages level progression.
- Functions:
  - `fetch_question(level: int) -> str`
  - `validate_answer(user_answer: str) -> bool`
  - `provide_hint() -> str`
  - `start_level(root, level, back_to_menu_callback)`

### 4️⃣ `main.py` (Game Entry Point)
- Initializes the Clock Game from the **Main Menu**.
- Supports **returning to the Main Menu** when exiting the game.

### 5️⃣ `run_game.py` (Standalone Execution)
- Allows the game to be launched manually **without the Main Menu**.

---

## 🖼️ Assets Folder
- **Contains important resources like:**
  - **UU-logo** (background image)
  - **progress.json** (stores game progress and leaderboard data)

---

## ⚠️ `__pycache__` Folder
- This folder is **automatically generated** when running Python scripts.
- It **stores compiled bytecode files** to speed up execution.
- You **can ignore or delete it**, but Python will regenerate it.

---

## 📌 Notes
- **Make sure `assets/progress.json` exists** before running the game.
- The **UU-logo should be in `assets/`** to avoid missing image errors.

---



