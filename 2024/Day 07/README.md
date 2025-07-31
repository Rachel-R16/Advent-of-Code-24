# Day 7: Bridge Repair

## Problem Description

### Part One
You are tasked with checking which equations could possibly be true by inserting operators (`+`, `*`) between numbers in a given list. You need to evaluate them left-to-right to see if they match a given target value (before the colon). The goal is to compute the sum of the test values from the equations that could be made true by inserting the correct operators.

### Part Two
A third operator (`||`) is introduced, which concatenates two numbers as strings (e.g., `12 || 345` becomes `12345`). You must now consider this operator along with `+` and `*` to find which equations could be true and compute their total calibration result.

## Solution Overview

### Input
- The input consists of several lines, each containing a target value followed by a list of numbers. Each number can be combined with the operators `+`, `*`, or `||` to match the target.

### Output
- For Part One: The sum of test values for the equations that can be made true by `+` and `*`.
- For Part Two: The sum of test values for the equations that can be made true by `+`, `*`, and `||`.

### Approach

#### Part One
1. Parse the input to extract the target value and list of numbers.
2. Use recursion to explore all possible combinations of `+` and `*` between numbers, evaluating from left to right.
3. If the combination matches the target value, include it in the sum for Part One.

#### Part Two
1. Modify the recursive solution to also consider the concatenation operator (`||`).
2. Evaluate all combinations of `+`, `*`, and `||` between the numbers, checking if any combination results in the target value.
3. Compute the new sum for Part Two.

### Part 1 Output:
```
Part 1 - Sum of valid equations with two operators: 1582598718861
```

### Part 2 Output:
```
Part 2 - Sum of valid equations with three operators: 165278151522644
```

## Conclusion
Both parts of the puzzle have been completed, with the sums calculated for equations that could be made true with the operators.
