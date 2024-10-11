# WaterSort Game 

## Overview
**WaterSort** is an engaging puzzle game where players sort colored water in tubes. The goal is to arrange the colors so that each tube contains only one color. This implementation includes various algorithms to solve the puzzle, such as Depth-First Search (DFS), Uniform Cost Search (UCS), Greedy Best-First Search, and A* Search. The program also compares different approaches and visually displays the solution path step-by-step with colored output.

## Features
- **Multiple Solving Algorithms**: Implementations of DFS, UCS, Greedy, and A* for solving the puzzle.
- **Interactive Output**: Visual representation of tubes and pouring actions directly in Jupyter Notebook.
- **Step-by-Step Solution Visualization**: Displays the path to the solution with color-coded output.
- **Performance Comparison**: Compares the efficiency of different algorithms based on node expansion and moves taken.

## Requirements
To run this game, you need:
- Anaconda 3 with Jupyter Notebook
- Required Python libraries:
  - `termcolor`
  - `pyparsing`
  - `tensorflow` (optional for advanced features)
  
Install the required libraries using pip:

  ```bash
  pip install termcolor pyparsing tensorflow
  ```
## Getting Started
1. Clone this repository to your local machine:
   
   ```bash
   git clone https://github.com/FarnoodID/WaterSort.git
   ```
2. Navigate to the project directory:

    ```bash
    cd WaterSort
    ```
3. Open Jupyter Notebook:
   
   ```bash
   jupyter notebook
   ```   
4. Open the `WaterSort.ipynb` file and run the cells to start the game.

## Game Mechanics
- The game begins with a set number of tubes filled with colored water.
- Players can pour water from one tube to another if the top colors match or if the destination tube is empty.
- The objective is to sort all colors into their respective tubes.

## Example Input
An example of the initial level input for starting the program is as follows:
```text
{{cyan}{blue}{blue}{yellow}}
{{green}{blue}{green}{yellow}}
{{cyan}{cyan}{magenta}{magenta}}
{{green}{magenta}{red}{red}}
{{red}{cyan}{yellow}{magenta}}
{{blue}{green}{red}{yellow}}
{{}{}{}{}}
{{}{}{}{}}
```
In this input, each set of curly braces represents a tube, and empty brackets indicate empty tubes.

## Algorithms Explained
### Depth-First Search (DFS)
Explores as far as possible along each branch before backtracking.

### Uniform Cost Search (UCS)
Expands nodes based on the lowest cost, ensuring optimal solutions when costs vary.

### Greedy Best-First Search
Uses a heuristic to prioritize nodes that appear closest to the goal.

### A* Search
Combines UCS and Greedy by considering both cost and heuristic estimates for optimal pathfinding.

## Performance Comparison
The efficiency of each algorithm is compared based on:
- **Nodes Expanded**: The number of nodes explored during execution.
- **Moves Count**: The number of moves taken from the initial state to reach the goal state.

| Algorithm | Nodes Expanded | Moves Count |
|-----------|----------------|-------------|
| DFS       | 73             | 19          |
| BFS       | 1684           | 10          |
| UCS       | 1684           | 10          |
| Greedy    | 87             | 10          |
| A*        | 87             | 10          |

## Conclusion
A* is generally the best algorithm when a suitable heuristic is chosen. While DFS uses less memory than BFS and UCS, it is not optimal. BFS has high space complexity, while Greedy can lead to local suboptimal solutions. A* effectively balances exploration and exploitation, making it a strong choice for solving this puzzle.


---
