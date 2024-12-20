# Day 16: Reindeer Maze

## Problem Description

### Part One
In the Reindeer Maze, the goal is to navigate from a start tile (marked 'S') to an end tile (marked 'E') while minimizing the total score. The Reindeer can move forward one tile at a time (increasing the score by 1 point) or rotate 90 degrees clockwise or counterclockwise (increasing the score by 1000 points). The Reindeer cannot move through walls, represented by '#'.

The challenge is to determine the lowest score a Reindeer could possibly get while traveling from the start to the end tile.

### Part Two
After calculating the lowest score for the best path in Part One, the next task is to figure out the best spot to sit. A tile is considered part of the best path if it is involved in any of the best paths (including the start and end tiles). The goal is to find how many non-wall tiles are part of at least one of the best paths through the maze.

## Solution Overview

### Input
The input consists of a grid representing the maze, where:
- '.' represents an open tile.
- '#' represents a wall.
- 'S' represents the start tile.
- 'E' represents the end tile.

### Output
The program outputs:
1. The lowest score a Reindeer can get to move from the start to the end tile (Part 1).
2. The number of tiles that are part of at least one of the best paths through the maze (Part 2).

### Approach
- **Part One**: We implement a variation of Dijkstra's algorithm, considering both the movement and direction changes. We track the distances for all possible states (position + direction), and use a priority queue to expand the shortest paths.
- **Part Two**: We calculate the best paths from both the start and the end using Dijkstra's algorithm. Then, we check all tiles to see if they are part of any best path by comparing the sum of the distances from the start and the end.

### Part 1 Output:
```
Part 1 - Lowest score a Reindeer can get: 95476
```

### Part 2 Output:
```
Part 2 - Tiles on at least one of the best paths: 511
```

## Conclusion
- **Part 1**: The Reindeer can achieve the lowest score of 95476 while navigating from the start to the end.
- **Part 2**: 511 tiles are part of at least one of the best paths through the maze.
