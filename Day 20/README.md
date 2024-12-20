# Day 20: Race Condition

## Problem Description

### Part One
In this puzzle, you are navigating a race track represented by a grid, where the goal is to find the fastest time from a start position ('S') to an end position ('E') while avoiding walls ('#'). Each move takes 1 picosecond. The program is allowed to cheat by passing through walls for up to 2 picoseconds to save time.

### Part Two
The rules change in Part Two, where the program can now cheat for up to 20 picoseconds. This opens up more possibilities for cheats and greater potential time savings. The task is to find all cheats that save at least 100 picoseconds.

## Solution Overview

### Input
The input is a grid representing the racetrack, where:
- `.` represents track
- `#` represents walls
- `S` is the start point
- `E` is the end point

### Output
The output should be the number of cheats that save at least 100 picoseconds for each part.

### Approach
1. **Dijkstra’s Algorithm**: Used to calculate the shortest distances from the start and end points to all other points on the grid.
2. **Cheating Mechanism**: By temporarily passing through walls, we calculate potential time savings and count the number of cheats that save at least 100 picoseconds.
3. **Manhattan Distance**: We use this to explore cells within a given range for potential cheats.

### Part 1 Output:
```
Part 1 - Num of cheats to save at least 100 picoseconds (dist 2): 1360
```

### Part 2 Output:
```
Part 2 - Num of cheats to save at least 100 picoseconds (dist 20): 1005476
```

## Conclusion
This puzzle challenges the program to navigate the race track in the least amount of time while utilizing a special "cheating" rule. By applying Dijkstra’s algorithm and exploring the various cheating options, we can determine how many cheats save at least 100 picoseconds in each part of the puzzle.
