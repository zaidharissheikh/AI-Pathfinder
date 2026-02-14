# AI Pathfinder: Uninformed Search Visualization

## 📌 Project Overview
This project implements an **AI Pathfinder** that visualizes how six different "blind" (uninformed) search algorithms explore a grid map. The application features a GUI built with Python's `tkinter` library, allowing users to place Start/Target nodes, draw walls, and watch the algorithms navigate in real-time.

The goal is to visualize the "thought process" of each algorithm—showing which nodes are added to the frontier, which are explored, and the final path chosen.

## 🚀 Features
* **6 Search Algorithms:** BFS, DFS, UCS, DLS, IDDFS, and Bidirectional Search.
* **Interactive Grid:** Set Start (S), Target (T), and Obstacle nodes manually.
* **Step-by-Step Visualization:**
    * **Orange:** Frontier nodes (in queue/stack).
    * **Numbered Orange:** Explored nodes (showing visit order 1, 2, 3...).
    * **Purple:** Final path from Start to Target.
* **Strict Movement Order:** Clockwise expansion (Up, Right, Bottom, Bottom-Right, Left, Top-Left).

## 🛠️ Prerequisites
* **Python 3.x** installed on your system.
* **Tkinter** (usually included with Python).
* No external libraries (like Pygame or NumPy) are required.

## 📥 Installation & Run Instructions

**Clone the Repository:**
```bash
git clone [https://github.com/zaidharissheikh/AI-Pathfinder.git](https://github.com/zaidharissheikh/AI-Pathfinder.git)
cd AI-Pathfinder
```
## 🎮 How to Use
* Select Algorithm: Choose a strategy (e.g., BFS, DFS) from the dropdown menu.

* Set Start & Target:

  * Click "Set Start (S)" and click a cell on the grid.

  * Click "Set Target (T)" and click a different cell.

* Draw Obstacles:

  * Click "Toggle Wall (-1)" and click/drag on the grid to draw walls.

* Run Search: Click "RUN SEARCH" to start the visualization.

* Reset: Use "Reset Grid" to clear everything or "Clear Path Only" to keep walls but remove the search visualization.

## 🧠 Algorithms Implemented
  * **Breadth-First Search (BFS):** Explores neighbors layer-by-layer. Guaranteed shortest path.
  
  * **Depth-First Search (DFS):** Explores as deep as possible before backtracking. Not optimal but memory efficient.
  
  * **Uniform-Cost Search (UCS):** Explores paths based on lowest cost (equivalent to BFS in this unweighted grid).
  
  * **Depth-Limited Search (DLS):** DFS with a depth limit to prevent infinite searching.
  
  * **Iterative Deepening DFS (IDDFS):** Repeated DLS with increasing limits (Depth 0, 1, 2...). Combines BFS optimality with DFS memory efficiency.
  
  * **Bidirectional Search:** Runs two simultaneous BFS searches (one from Start, one from Target) until they meet.
## ⚠️ Known Constraints
  * Movement: The agent moves in 6 directions (Clockwise + Top-Left/Bottom-Right diagonals). It strictly ignores Top-Right and Bottom-Left diagonals as per assignment instructions.
