# Day 8: Resonant Collinearity

## Problem Description

### Part One
You find yourself on the roof of a top-secret Easter Bunny installation, surrounded by antennas emitting a signal that increases the likelihood of people purchasing Easter Bunny brand Imitation Mediocre Chocolate as a Christmas gift. The antennas are tuned to specific frequencies and are scattered across the city. An antinode occurs at any point that is perfectly in line with two antennas of the same frequency, where one antenna is twice as far away as the other. The goal is to calculate how many unique locations within the bounds of the map contain an antinode.

### Part Two
After revisiting the model, it turns out that an antinode occurs at any grid position exactly in line with at least two antennas of the same frequency, regardless of distance. This means that even the positions of the antennas themselves become antinodes. The goal is to calculate the total number of unique locations within the bounds of the map that contain an antinode, including the positions of the antennas.

## Solution Overview

### Input
The input consists of a grid representing the city, with each antenna denoted by a lowercase letter, uppercase letter, or digit. Empty grid spaces are represented by `.`.

### Output
The program outputs:
1. The number of unique locations containing an antinode for Part 1.
2. The number of all locations containing antinodes (including duplicates) for Part 2.

### Approach
- **Part One**: First, the antennas are identified and sorted. For each pair of antennas with the same frequency, the positions between them are calculated, considering both the absolute distance and the direction. The resulting antinodes are added to a set to ensure uniqueness.
- **Part Two**: The updated model includes all positions of antennas as antinodes, along with any points between antennas that align in a straight line. The resulting antinodes are stored, ensuring that all positions are counted, including duplicates.

### Part 1 Output:
```
Part 1 - Number of distinct antinodes: 303
```

### Part 2 Output:
```
Part 2 - Number of all antinodes: 1045
```

## Conclusion
- **Part 1**: The number of unique antinodes is calculated by finding positions that are in line with at least two antennas of the same frequency, while considering the distance between them.
- **Part 2**: The updated model accounts for all positions that are in line with at least two antennas of the same frequency, including the positions of the antennas themselves, resulting in a larger total of antinodes.
