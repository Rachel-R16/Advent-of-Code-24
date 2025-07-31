# Day 21: Keypad Conundrum

## Problem Description

### Part One
To rescue a missing Historian, a numeric keypad is used to unlock a door by typing specific codes. However, robots must use directional keypads to maneuver their arms to type the codes, starting at the `A` button of the keypads. The challenge is to determine the shortest sequence of button presses needed to type the door codes and compute the sum of complexities for all codes.

**Complexity Calculation**:
- Multiply the length of the shortest sequence to type a code by the numeric portion of the code.
- Sum the complexities for all the codes.

### Part Two
A second Historian is trapped, but this time 25 directional keypads are involved in the chain. The task remains the same, but the number of keypads significantly increases the challenge. Compute the sum of complexities for all codes under this new setup.

## Solution Overview

### Input
- A list of door codes (e.g., `029A`, `980A`, etc.).

### Output
- **Part 1**: Sum of the complexities of the codes with 2 directional keypads.
- **Part 2**: Sum of the complexities of the codes with 25 directional keypads.

### Approach
1. Map the numeric keypad and directional keypad into coordinate grids.
2. Define a function to compute transitions between keys, considering boundary restrictions.
3. For each code, calculate the required transitions for the numeric keypad.
4. Simulate the chain of directional keypads and update transitions iteratively.
5. Compute the complexity by multiplying the total number of transitions by the numeric part of the code.
6. Sum complexities for all codes.

## Example Output

### Part 1 Output:
```
Part 1 - Sum of the complexities of the five codes (2 direction pads): 169390
```

### Part 2 Output:
```
Part 2 - Sum of the complexities of the five codes (25 direction pads): 210686850124870
```

## Conclusion
- **Part 1**: The solution involved calculating complexities using two directional keypads. The total complexity was relatively manageable.
- **Part 2**: The increased number of directional keypads significantly amplified the complexity, demonstrating the scalability of the approach.
