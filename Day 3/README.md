# Day 3: Mull It Over

## Problem Description

### Part One
The corrupted memory in the computer is full of instructions to multiply numbers, but the data is jumbled with invalid characters. Your task is to scan the memory for valid `mul(X, Y)` instructions, ignore any invalid characters, and sum up the results of the multiplications.

For example, given the input:
```
xmul(2,4)%&mul[3,7]!@^do_not_mul(5,5)+mul(32,64]then(mul(11,8)mul(8,5))
```
The valid multiplication operations are:
- `mul(2,4)` → 2 * 4 = 8
- `mul(5,5)` → 5 * 5 = 25
- `mul(11,8)` → 11 * 8 = 88
- `mul(8,5)` → 8 * 5 = 40

The total sum of these multiplications is 161.

### Part Two
The engineers have introduced two new instructions:
- `do()` which enables future `mul()` instructions.
- `don't()` which disables future `mul()` instructions.

At the beginning of the program, all `mul()` instructions are enabled. If a `don't()` instruction appears, it disables future multiplications until a `do()` instruction is encountered.

For example, given the input:
```
xmul(2,4)&mul[3,7]!^don't()_mul(5,5)+mul(32,64](mul(11,8)undo()?mul(8,5))
```
The valid multiplication operations are:
- `mul(2,4)` → 2 * 4 = 8
- `mul(8,5)` → 8 * 5 = 40

The total sum of these multiplications is 48.

## Solution Overview

### Input
The input consists of corrupted memory that contains a series of characters, including valid and invalid `mul(X, Y)` instructions, along with `do()` and `don't()` commands.

### Output
The program outputs:
1. The total sum of products for Part 1 based on valid `mul(X, Y)` instructions.
2. The total sum of products for Part 2, considering the `do()` and `don't()` instructions to enable and disable `mul()` operations.

### Approach
- **Part One**: Extract valid `mul(X, Y)` instructions, ignoring invalid characters, and sum up the multiplication results.
- **Part Two**: Process the `do()` and `don't()` instructions to enable or disable future `mul()` instructions and sum up the valid multiplications.

### Part 1 Output:
```
Part 1 - Sum:  192767529
```

### Part 2 Output:
```
Part 2 - Sum-Filtered:  104083373
```

## Conclusion
- **Part 1**: We scanned the corrupted memory for valid `mul(X, Y)` instructions, multiplied the valid pairs, and summed the results to get the total of 192767529.
- **Part 2**: We considered the `do()` and `don't()` instructions to enable or disable future `mul(X, Y)` instructions, and summed the results of the enabled multiplications to get the total of 104083373.
