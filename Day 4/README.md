# Day 4: Ceres Search

## Problem Description

### Part One
You are tasked with searching for the word "XMAS" in a grid of characters. The word can appear in any direction: horizontally, vertically, diagonally, and even backward. You need to count how many times the word "XMAS" appears in the grid.

Given a grid, such as:
```
MMMSXXMASM
MSAMXMSMSA
AMXSXMAAMM
MSAMASMSMX
XMASAMXAMM
XXAMMXXAMA
SMSMSASXSS
SAXAMASAAA
MAMMMXMMMM
MXMXAXMASX
```
You need to find and count all the occurrences of the word "XMAS". In this example, the word appears 18 times.

### Part Two
In this part, the puzzle introduces a new pattern, "X-MAS". You need to find two instances of the word "MAS" in the shape of an "X". For example:
```
M.S
.A.
M.S
```
You need to identify how many times this shape appears in the grid.

### Solution Overview

### Input
The input is a grid of characters where the word "XMAS" and the "X-MAS" shape are to be searched for.

### Output
The program outputs:
1. The count of occurrences of "XMAS" in all directions for Part 1.
2. The count of "X-MAS" shapes for Part 2.

### Approach
- **Part One**: Search for the word "XMAS" in all possible directions (horizontal, vertical, diagonal, and reversed).
- **Part Two**: Identify and count the "X-MAS" shape by searching for two "MAS" instances that form an "X" around a central "A".

### Part 1 Output:
```
Part 1 - Count of XMAS: 2464
```

### Part 2 Output:
```
Part 2 - Count of X-MAS: 1982
```

## Conclusion
- **Part 1**: We counted all occurrences of the word "XMAS" in the grid by checking all directions and ensuring the word fits at each position. The result was 2464 occurrences.
- **Part 2**: We searched for the "X-MAS" shape, where two "MAS" patterns form an "X" around a central "A". The result was 1982 occurrences.
