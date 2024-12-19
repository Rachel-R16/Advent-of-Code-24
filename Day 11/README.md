# Day 11: Plutonian Pebbles

## Problem Description

The ancient civilization on Pluto left behind a strange set of stones, each engraved with a number. These stones exhibit unusual behavior when blinked at. Every time you blink, the stones change based on the following rules:

1. **Rule 1**: If the stone is engraved with the number 0, it is replaced by a stone engraved with the number 1.
2. **Rule 2**: If the stone is engraved with a number that has an even number of digits, it is replaced by two stones. The left half of the digits are engraved on the new left stone, and the right half of the digits are engraved on the new right stone.
3. **Rule 3**: If none of the above rules apply, the stone is replaced by a new stone where its number is multiplied by 2024.

The task is to observe how the stones evolve after several blinks, and calculate how many stones there are after 25 and 75 blinks.

### Part One
You need to calculate how many stones will be present after blinking the stones 25 times.

### Part Two
You need to calculate how many stones will be present after blinking the stones 75 times.

## Solution Overview

The solution employs recursion and memoization to efficiently calculate the number of stones after a given number of blinks. The `count_blinks` function is implemented using the `@cache` decorator to store previously computed results for efficiency. The core logic checks if the stone should split, multiply by 2024, or change based on the rules defined in the problem description.

### Input

- A list of integers, each representing the number engraved on a stone.

### Output

- **Part 1**: The total number of stones after blinking 25 times.
- **Part 2**: The total number of stones after blinking 75 times.

### Approach

1. **Memoized Recursive Calculation**: The function `count_blinks` recursively calculates the number of stones after a given number of blinks. It applies the rules for splitting, multiplying, or changing the stones based on their length and value.
2. **Base Case**: When the number of blinks reaches 0, the function returns 1, as no more changes occur.
3. **Recursive Steps**:
   - If the stone’s length is even, it is split into two stones, and the process is repeated for both parts.
   - If the length is odd, the stone’s value is multiplied by 2024, and the recursion continues.
4. **Final Calculation**: For both parts, the sum of the results from all initial stones is calculated.

### Part 1 Output:
```
Part 1 - Number of stones after blinking 25 times: 216996
```

### Part 2 Output:
```
Part 2 - Number of stones after blinking 75 times: 257335372288947
```

## Conclusion

This challenge involves simulating the evolution of stones based on defined transformation rules. The solution efficiently handles recursion with memoization to compute the number of stones after 25 and 75 blinks, utilizing the three rules that govern how each stone changes.
