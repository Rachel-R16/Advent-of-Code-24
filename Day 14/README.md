# Day 14: Restroom Redoubt

## Problem Description
### Part One
One of The Historians needs to use the bathroom at Easter Bunny Headquarters (EBHQ). However, the bathroom area is surrounded by robots moving in predictable straight lines within a bounded grid. Robots have current positions and velocities, and they teleport when crossing grid boundaries, effectively wrapping around.

The task is to predict robot positions after 100 seconds and determine the safety factor by counting the number of robots in each quadrant of the grid. Robots exactly in the middle horizontally or vertically do not count towards any quadrant. The safety factor is calculated as the product of robot counts in all quadrants.

### Part Two
The robots may occasionally align to form a picture of a Christmas tree. The task is to determine the minimum number of seconds required for this pattern to appear.

## Solution Overview
### Input
The input contains multiple lines, each describing a robot's position and velocity:
```
p=x1,y1 v=dx1,dy1
p=x2,y2 v=dx2,dy2
...
```
- `p=x,y` represents the robot’s current position.
- `v=dx,dy` represents the robot’s velocity per second.
- The grid dimensions are `101 x 103` tiles.

### Output
- **Part One:** The safety factor after 100 seconds.
- **Part Two:** The minimum number of seconds for the robots to form a Christmas tree pattern.

### Approach
#### Part One
1. **Simulation:** Update each robot’s position based on its velocity, applying wrap-around logic for grid boundaries.
2. **Quadrant Assignment:** Assign robots to quadrants based on their positions relative to the grid center, excluding robots in the middle.
3. **Safety Factor Calculation:** Count robots in each quadrant and compute the product of these counts.

#### Part Two
1. Simulate robot movements iteratively.
2. Check for alignment that resembles a Christmas tree pattern by visual inspection of grid states.
3. Return the time step at which the pattern appears.

### Part 1 Output:
```
Part 1 - Safety factor after 100 seconds: 229632480
```

### Part 2 Output:
```
Part 2 - Fewest number of seconds to display Christmas Tree: 7051
```

## Conclusion
This problem involved simulating movement within a bounded grid and applying modular arithmetic for wrap-around effects. It required efficient counting and pattern recognition to compute the safety factor and detect a specific arrangement of robots.

