# Day 6: Guard Gallivant

## Problem Description

### Part One
The Historians have whisked you to the year 1518, where a guard is patrolling a lab at the North Pole. Your task is to predict the guard's movements based on their protocol, which involves turning right when an obstacle is in front and stepping forward when there is no obstruction. You need to determine how many distinct positions the guard will visit before leaving the mapped area.

### Part Two
After analyzing the guard's movements in Part One, you need to identify all possible positions where you can place a new obstruction, causing the guard to get stuck in a loop. The new obstruction must not be placed at the guard's starting position. The goal is to find how many different positions can be used for this obstruction to get the guard stuck in a loop.

## Solution Overview

### Input
The input consists of a grid representing the lab, where:
- `.` represents an empty space.
- `#` represents an obstruction.
- `^`, `v`, `<`, or `>` represent the guard's initial direction (up, down, left, or right, respectively).

### Output
1. For Part One, the program outputs the number of distinct positions visited by the guard before leaving the mapped area.
2. For Part Two, the program outputs the number of possible positions where a new obstruction can be placed to get the guard stuck in a loop.

### Approach
- **Part One**: The guard moves according to a strict protocol, turning right if an obstacle is ahead, and stepping forward if not. We simulate the guard’s movement on the grid and track the number of distinct positions visited.
- **Part Two**: After identifying all visited positions, we check where placing a new obstruction would cause the guard to get stuck in a loop, counting how many such positions are possible.

### Part 1 Output:
```
Part 1 - Distinct cells visited: 4988
```

### Part 2 Output:
```
Part 2 - Total loops counted: 1697
```

## Conclusion
- **Part 1**: The program tracks the guard's movements, and we determined that the guard visited 4988 distinct positions before leaving the area.
- **Part 2**: By analyzing the guard’s movement pattern, we found 1697 positions where adding a new obstruction would cause the guard to get stuck in a loop.
