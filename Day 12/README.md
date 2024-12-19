# Day 12: Garden Groups

## Problem Description

The Historians are near a massive garden with multiple garden plots, each growing a specific type of plant. These plots are grouped into regions where adjacent plots (horizontally or vertically) growing the same type of plant are part of the same region. 

Your task is to calculate the cost of fencing required for each region. There are two ways to calculate the cost:

### Part One
The price of fencing for each region is determined by multiplying its area (the number of plots) by its perimeter (the number of sides that are exposed to the outside).

### Part Two
In this part, the price of fencing is calculated using the number of sides of the fence required to enclose the region, instead of its perimeter. A side is considered only if it is not adjacent to another plot in the same region.

### Example:
For a given garden map:

```
AAAA
BBCD
BBCC
EEEC
```

- The region of type A has an area of 4 and a perimeter of 10, resulting in a fence price of 40.
- The region of type B has an area of 4 and a perimeter of 8, resulting in a fence price of 32.
- The region of type C has an area of 4 and a perimeter of 10, resulting in a fence price of 40.
- The region of type D has an area of 1 and a perimeter of 4, resulting in a fence price of 4.
- The region of type E has an area of 3 and a perimeter of 8, resulting in a fence price of 24.

The total price for this example is 140.

## Solution Overview

The solution uses a depth-first search (DFS) approach to group adjacent plots into regions, and then calculates the area and the cost for each region using either the perimeter or the number of sides. 

### Key Functions:
1. **create_individual_plots**: This function processes the garden layout to identify connected regions and their respective fence boundaries. It returns a list of plots along with their fences.
2. **calculate_area_and_perimeters**: This function calculates the cost of fencing for each region based on its area and perimeter.
3. **calculate_area_and_sides**: This function calculates the cost of fencing based on the number of sides for each region.

### Input

- A garden layout, where each garden plot is labeled with a specific letter indicating the type of plant. The garden is represented as a 2D grid.

### Output

- **Part 1**: The total cost of fencing all regions using the perimeter-based pricing.
- **Part 2**: The total cost of fencing all regions using the side-based pricing.

### Approach

1. **Parsing the Garden Layout**: The garden map is read from an input file and mapped to a set of coordinates based on each plant type.
2. **Region Identification**: Connected plants of the same type are grouped into regions using a DFS approach.
3. **Cost Calculation**:
   - For Part 1, the cost is calculated by multiplying the area of each region by its perimeter.
   - For Part 2, the cost is calculated by multiplying the area of each region by the number of sides.

### Part 1 Output:
```
Part 1 - Cost with perimeter and area: 1437300
```

### Part 2 Output:
```
Part 2 - Cost with side and area: 849332
```

## Conclusion

The challenge required simulating a garden map with connected regions, calculating costs based on different criteria (perimeter vs. sides). The solution efficiently groups the regions and computes the required costs, addressing both parts of the puzzle.
