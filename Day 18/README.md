# Day 18: RAM Run

## Problem Description
You and The Historians are trapped inside a pixelated world inside a computer. The task is to navigate through a memory space corrupted by falling bytes. The goal is to find the minimum number of steps to reach the exit, avoiding corrupted memory spaces, and later determine the first corrupted space that blocks the path.

### Part One
Simulate the falling of 1024 bytes into the memory space. Each byte marks the memory space as corrupted. After the corruption, calculate the minimum number of steps required to reach the exit.

### Part Two
Simulate further corruption and find the first corrupted byte that blocks the path to the exit. This will be the first byte that prevents you from reaching the bottom-right corner.

## Solution Overview

### Input
The input consists of a list of byte positions (coordinates) that will fall into the memory space, corrupting the corresponding memory coordinates.

### Output
- Part One: The minimum number of steps required to reach the exit after 1024 bytes have corrupted the memory.
- Part Two: The coordinates of the first corrupted byte that blocks the path to the exit.

### Approach
1. **Kilobyte Corruption**: A function (`kilobyte_corrupted`) marks the specified coordinates as corrupted in the memory space. This function updates the grid accordingly after each byte is simulated to fall.
2. **Shortest Path Calculation**: A breadth-first search (BFS) function (`shortest_path`) is used to calculate the minimum number of steps required to reach the exit from the top-left corner (0, 0).
3. **Simulation of Corruption**: The `simulate_corrupting` function iterates over the corrupted memory spaces and finds the first corrupted byte that blocks the exit. This is determined by checking if the path to the exit becomes blocked after each byte falls.

### Part 1 Output:
```
Part 1 - Steps to exit after a kilobyte of corrupted spaces: 310
```

### Part 2 Output:
```
Part 2 - Co-ord that closes exit: (16, 46)
```

## Conclusion
This solution simulates the corrupting memory space and determines the minimum number of steps to exit. Additionally, it finds the first byte that prevents a successful exit, allowing the simulation to cover both parts of the puzzle.

