# Day 25: Code Chronicle

## Problem Description
You are given schematics for virtual five-pin tumbler locks and keys. Each schematic consists of a grid where `#` represents a pin or a part of a key, and `.` represents an empty space. The task is to determine how many unique lock/key pairs can fit together without overlapping any pins. A lock is identified by a top row filled with `#` and a bottom row filled with `.`. A key has the reverse, with a top row filled with `.` and a bottom row filled with `#`. The locks and keys can be represented as columns of varying heights.

## Solution Overview
The solution involves parsing the lock and key schematics from an input file, calculating the height of pins for each lock and key, and checking whether any lock and key pair fits together without overlapping pins in any column. The heights are calculated based on the `#` characters in the schematic, and each lock/key pair is checked to ensure that the sum of the pin heights in any column does not exceed 5.

### Input
The input consists of several lock and key schematics in a file named `D25 Input`. Each schematic is a 5xN grid representing either a lock or a key. The top and bottom rows of each schematic help determine whether it is a lock or a key. Locks have `#` on the top and `.` on the bottom, while keys have `.` on the top and `#` on the bottom. Schematics are separated by blank lines.

### Output
The output is a single integer representing the number of unique lock/key pairs that fit together without overlapping. A lock/key pair fits if the sum of the corresponding heights in each column is less than or equal to 5.

### Approach
1. **Parse the Input**: Read the input file line by line, separating schematics into locks and keys based on the top and bottom rows.
2. **Calculate Heights**: For each lock and key, calculate the heights of the pins/columns by counting the `#` characters in each column.
3. **Check Fit**: For each lock, check it against each key to see if the heights in all columns fit together (i.e., the sum of the corresponding heights in each column is less than or equal to 5).
4. **Count Valid Pairs**: Count how many lock/key pairs fit without overlapping.

### Part 1 Output:
```
Part 1 - Unique lock/key pairs without overlapping: 2618
```

## Conclusion
This solution successfully solves the problem of determining how many unique lock/key pairs fit together based on their pin heights. The algorithm efficiently parses the input, calculates the pin heights, and checks all combinations to count valid lock/key pairs.
