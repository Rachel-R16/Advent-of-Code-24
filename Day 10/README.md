# Day 10: Hoof It

## Problem Description

You arrive at a Lava Production Facility on a floating island in the sky. You discover a reindeer holding a book titled "Lava Island Hiking Guide," but most of it is scorched. The reindeer hands you a blank topographic map of the surrounding area, and you must help fill in the missing hiking trails.

The map indicates the height at each position using a scale from 0 (lowest) to 9 (highest). A hiking trail starts at height 0, ends at height 9, and increases by exactly 1 at each step. Hiking trails move up, down, left, or right — no diagonals.

A trailhead is any position that starts one or more hiking trails (these positions have height 0). The trailhead's score is the number of 9-height positions reachable from that trailhead via a hiking trail.

### Part One
You need to calculate the sum of the scores of all trailheads on the topographic map.

### Part Two
A trailhead's rating is the number of distinct hiking trails that begin at that trailhead. Calculate the sum of the ratings of all trailheads on the map.

## Solution Overview

This solution implements the following steps:

1. **Input Parsing**: The topographic map is read from a file and converted into a 2D grid of integers, where each integer represents the height at that position.
2. **Neighbor Exploration**: For each trailhead (position with height 0), we find all reachable positions with a height of 1 greater than the current position, recursively.
3. **Path Calculation**: The hiking paths are explored, and the score and rating are calculated based on the number of reachable 9's and distinct paths from each trailhead.
4. **Final Calculation**: The sum of scores and ratings is printed for both parts.

### Input

- A file containing the topographic map of the area. Each line represents a row of the map, with each character representing a height (from 0 to 9).

### Output

- **Part 1**: The sum of the scores of all trailheads on the map.
- **Part 2**: The sum of the ratings of all trailheads.

### Approach

- **Part 1**: We start at each trailhead (height 0) and explore all reachable 9's, counting the total number of 9's reachable from each trailhead.
- **Part 2**: We find all distinct paths starting from each trailhead (height 0), ensuring that each path only steps to neighboring cells with a height of exactly 1 greater than the current position. We then count the total number of distinct hiking trails from each trailhead.

### Part 1 Output:
```
Part 1 - Sum of the scores of all trailheads: 744
```

### Part 2 Output:
```
Part 2 - Sum of the ratings of all trailheads: 1651
```

## Conclusion

The challenge involves finding hiking trails based on topography and calculating the trailhead scores and ratings by exploring all possible paths starting from height 0 and reaching height 9. The solution uses recursive search techniques to explore neighboring positions and compute the desired outputs.

