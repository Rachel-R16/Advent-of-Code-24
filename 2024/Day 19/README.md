# Day 19: Linen Layout

## Problem Description

In this puzzle, you're tasked with helping The Historians at an onsen, where the staff needs help arranging towels. The towels have specific patterns made from colored stripes, and the goal is to determine how many different ways you can arrange available towel patterns to match a desired design. The towels can be used multiple times to form a design, but each design must exactly match the desired sequence.

### Part One
You are given a list of available towel patterns and desired designs. Your task is to calculate how many designs can be made using the available towel patterns.

### Part Two
After calculating how many designs are possible, you need to compute how many different ways each design can be formed using the towel patterns. You should sum the total number of ways to form each design.

## Solution Overview

### Input
The input consists of:
- A list of available towel patterns (each pattern is a string of stripes).
- A list of desired designs (each design is a string of stripes that needs to be matched exactly using the available towel patterns).

### Output
- **Part One**: The number of designs that can be formed using the available towel patterns.
- **Part Two**: The sum of all possible ways to form each design using the available towel patterns.

### Approach

1. **Towel Pattern Matching**: The `check_design` function is a recursive function that checks if a design can be formed using the available towel patterns. It utilizes caching (`@cache`) to optimize performance by storing previously calculated results.
   
2. **Count Possible Patterns**: The `possible_patterns` function calculates how many designs can be formed from the available towel patterns. It does this by calling `check_design` for each design and counting how many of them return a positive result (i.e., they can be formed).

3. **Sum of Pattern Possibilities**: The `pattern_possibilities` function calculates the total number of ways each design can be formed. It sums up all the possibilities for each design.

### Part 1 Output:
```
Part 1 - Total possible patterns from the given towels are: 315
```
### Part 2 Output:
```
Part 2 - Sum of different pattern possibilities: 625108891232249
```
## Conclusion
This solution efficiently calculates the possible towel arrangements for each design and determines the number of different ways to form each design using dynamic programming and memoization.
