# Day 1: Historian Hysteria

## Problem Description

### Part One
The Chief Historian's office is filled with lists of historically significant locations, identified by unique location IDs. The goal is to compare two lists of location IDs and determine the total distance between them. The lists are compared by pairing up corresponding numbers after sorting both lists in ascending order and then computing the absolute differences between the paired numbers. The final result is the sum of these differences.

### Part Two
After analyzing the first part, we find that many location IDs appear in both lists. To calculate a total similarity score, each number in the left list is multiplied by the number of times it appears in the right list. The result is a weighted sum of these products.

## Solution Overview

### Input
The input consists of two lists of integers: the first list (left list) and the second list (right list). Both lists contain historical location IDs.

### Output
The program outputs:
1. The total distance between the left and right lists by summing up the absolute differences between corresponding elements in the sorted lists.
2. The total similarity score by multiplying each element in the left list by its frequency in the right list and summing up these products.

### Approach
- **Part One**: The lists are sorted, and the absolute differences between corresponding elements are calculated.
- **Part Two**: The frequency of each element in the right list is counted, and the total similarity score is computed by multiplying each element in the left list by its frequency in the right list.


### Part 1 Output:
```
Part 1 - Sum of Differences: 11
```

### Part 2 Output:
```
Part 2 - Frequency Sum: 31
```

## Conclusion
- **Part 1**: We calculated the total distance by summing the absolute differences between paired numbers.
- **Part 2**: We computed the total similarity score by considering the frequency of each number in both lists.
