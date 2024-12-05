# Day 2: Red-Nosed Reports

## Problem Description

### Part One
The engineers at the Red-Nosed Reindeer nuclear fusion/fission plant are analyzing unusual data from their reactor. The data consists of multiple reports, each containing a series of numbers (levels). A report is considered safe if:
1. The numbers are either strictly increasing or strictly decreasing.
2. The difference between each pair of adjacent levels is at least 1 and at most 3.

The task is to determine how many of the reports are safe by applying the above rules.

### Part Two
The engineers discover that a module called the Problem Dampener allows them to remove a single bad level from an unsafe report, potentially making it safe. After this adjustment, the same rules for determining safety apply. The challenge is to figure out how many reports are now safe after applying the Problem Dampener.

## Solution Overview

### Input
The input consists of several reports, each with a series of space-separated integers representing the levels.

### Output
The program outputs:
1. The total number of reports that are safe, based on the criteria from Part 1.
2. The total number of reports that are safe either as-is or by removing one level, based on the criteria from Part 2.

### Approach
- **Part One**: Check each report to see if it is strictly increasing or decreasing and if the differences between adjacent numbers are within the allowed range.
- **Part Two**: If a report is unsafe, attempt to remove one level and check if the resulting report becomes safe.

### Part 1 Output:
```
Part 1 - Safe: 224
```

### Part 2 Output:
```
Part 2 - Fixed + Safe: 293
```


## Conclusion
- **Part 1**: The number of reports that adhere to the safety criteria without modification is 224.
- **Part 2**: The number of reports that can be made safe by removing a single level is 293.

