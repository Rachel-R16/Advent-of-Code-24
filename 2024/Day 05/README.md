# Day 5: Print Queue

## Problem Description

### Part One
In the North Pole printing department, the safety manual updates must follow strict page ordering rules. Given a set of rules where `X|Y` means page `X` must appear before page `Y` if both are present in an update, determine which updates are already correctly ordered.

For updates that are correctly ordered:
- Identify the middle page number from each update.
- Compute the sum of these middle page numbers.

### Part Two
For updates that are not correctly ordered:
- Fix their order according to the given rules.
- Identify the middle page number from each corrected update.
- Compute the sum of these middle page numbers.

## Solution Overview

### Input
The input consists of two sections:
1. **Rules**: A series of ordering rules in the format `X|Y`, specifying that `X` must come before `Y` if both are present.
2. **Pages**: A list of updates, each containing a series of page numbers.

### Output
The program outputs:
1. The sum of middle page numbers from updates that are already correctly ordered.
2. The sum of middle page numbers from updates that are corrected to follow the rules.

### Approach
1. Parse the input into two structures:
   - A dictionary mapping page numbers to their ordering constraints.
   - A list of page updates.
2. For each update:
   - Check if it adheres to the ordering rules.
   - If correct, add its middle page number to the sum for Part 1.
   - If incorrect, reorder it using the rules, then add its middle page number to the sum for Part 2.
3. Output the computed sums for both parts.

### Part 1 Output:
```
Part 1 - Sum of correctly ordered: 4959
```

### Part 2 Output:
```
Part 2 - Sum of incorrectly ordered: 4655
```

## Conclusion
- **Part 1**: We identified correctly ordered updates and computed the sum of their middle page numbers.
- **Part 2**: We corrected incorrectly ordered updates, computed their middle page numbers, and summed them. This ensured all updates adhered to the ordering rules.
