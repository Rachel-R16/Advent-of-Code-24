# Day 15: Warehouse Woes

## Problem Description

You are inside a mini-submarine that is navigating a warehouse complex, controlled by a malfunctioning robot. The robot moves around pushing boxes, and your task is to predict the robot's movements, then calculate the final GPS coordinates of the boxes in the warehouse. 

- The robot starts at a given position (`@`).
- The warehouse layout is represented by a grid with walls (`#`), boxes (`O`), and empty spaces (`.`).
- The robot follows a sequence of movements (`^`, `v`, `<`, `>`), attempting to push the boxes if they are in its way. However, the robot cannot push boxes into walls.

After the robot finishes its movements, you are to calculate the sum of the GPS coordinates of all boxes (`O`) in the warehouse. The GPS coordinate of a box is calculated as `100 * row + col`, where `row` and `col` are the box's position on the grid.

In the second part of the problem, the warehouse is scaled by doubling the width, and the robot's behavior is the same. You are asked to calculate the new GPS coordinates for this enlarged warehouse.

## Solution Overview

### Part One:
- The warehouse is modeled as a grid.
- A sequence of movements is given, and the robot moves accordingly, attempting to push boxes.
- After all movements, the sum of GPS coordinates for all boxes is calculated.

### Part Two:
- The warehouse layout is enlarged by doubling its width.
- The robot's movements are simulated in the enlarged layout.
- The sum of GPS coordinates for the boxes is calculated again in the enlarged warehouse.

### Input

The input consists of:
1. A grid representing the warehouse with walls (`#`), boxes (`O`), empty spaces (`.`), and the robot (`@`).
2. A series of movements (`^`, `v`, `<`, `>`) that the robot will attempt to make.

## Output

The output consists of two parts:
1. The sum of all boxes' GPS coordinates after the robot finishes moving in the original warehouse.
2. The sum of all boxes' GPS coordinates after the robot finishes moving in the enlarged warehouse.

### Approach

1. **Room Representation**: The warehouse is represented as a grid where each character corresponds to a type of space (wall, box, or empty).
2. **Movement Simulation**: The robot attempts to move according to the instructions. If a box is in its way, it attempts to push the box. If a box or robot would move into a wall, the move is ignored.
3. **GPS Calculation**: After the robot finishes moving, the coordinates of the boxes are used to calculate the sum of their GPS values.

### Part 1 Output:
```
Part 1 - Find GPS of boxes in room: 1406392
```

### Part 2 Output:
```
Part 2 - Find GPS of boxes in enlarged room: 1429013
```

## Conclusion

The puzzle tests your ability to simulate robot movements in a grid and calculate values based on positions. It also introduces the concept of enlarging the grid and adjusting movement logic.
