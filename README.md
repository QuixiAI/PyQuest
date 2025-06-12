# PyQuest

**An interactive, REPL-native journey to learn Python by doing.**  
Inspired by [Gameshell](https://github.com/phyver/GameShell), but designed entirely within the Python REPL.

---

## 📜 What Is This?

**PyREPLQuest** is a gamified curriculum that teaches Python *from the inside out* — through hands-on problem-solving, inside the Python REPL. Each level presents a challenge. When you solve it, you advance. Your progress is saved automatically.

---

## 🚀 Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/yourusername/pyreplquest.git
cd pyreplquest
````

### 2. Start Python REPL

```bash
python
```

### 3. Start the game

Inside the REPL:

```python
from game.engine import start_game
start_game()
```

---

## 🧠 How It Works

* Each level is a separate Python file located in `levels/`.
* When the level loads, it calls `print_goal()` to display your objective.
* You solve the challenge using Python code in the REPL.
* Run `check()` to test your solution.
* If correct, you automatically advance to the next level.
* Your progress is saved in `save/player_progress.json`.

---

## 📦 Project Structure

```
pyreplquest/
│
├── game/                # Core game engine
│   ├── engine.py
│   ├── state.py
│   └── ...
│
├── levels/              # One Python file per level
│   ├── level01.py
│   ├── level02.py
│   └── ...
│
├── save/                # Stores progress
│   └── player_progress.json
│
├── main.py              # (Optional) Entry point
└── README.md
```

---

## 📘 Sample Level

Here’s what a typical level file looks like (`levels/level01.py`):

```python
def print_goal():
    print("Define a variable `name` with your name as a string.")

def check_complete(state):
    return isinstance(state.get("name"), str) and len(state["name"]) > 0
```

You’d solve it like this in the REPL:

```python
>>> name = "Ada"
>>> check()
✅ Level complete!
```

---

## 🎯 Learning Progression

PyREPLQuest starts with basic syntax, and gradually builds toward real-world projects like:

* File I/O (text, JSON, CSV)
* Data transformation (ETL)
* Search and sort algorithms
* Visualization with matplotlib
* Simple Flask web apps
* SQLite database operations

All playable *entirely from the REPL*.

---

## 🛠 Requirements

* Python 3.8+
* No external dependencies until charting/web levels
* Install optional libraries for advanced levels:

  ```bash
  pip install matplotlib flask requests
  ```

---

## 🧑‍💻 Who Is This For?

* Homeschooling parents or educators
* Kids, teens, or adults learning Python
* REPL lovers
* Fans of Gameshell-style learning

---

## 📅 License

MIT License. Designed to be forked, modified, and shared.
