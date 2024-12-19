Here is the README formatted according to your specifications:

---

# Day 13: Claw Contraption

## Problem Description

### Part One
In a tropical resort's arcade, claw machines are controlled by buttons `A` and `B`. Button `A` moves the claw a specific amount along the X and Y axes and costs 3 tokens per press, while button `B` does the same but costs 1 token per press. To win a prize, the claw must reach the exact X and Y coordinates of the prize.

The task is to determine the minimum tokens required to win as many prizes as possible, considering the button configurations for each claw machine.

### Part Two
Due to a measurement error, the X and Y coordinates of all prizes are increased by \(10^{13}\). The goal is to find the minimum tokens required to win as many prizes as possible under these updated conditions.

## Solution Overview

### Input
- Button configurations (`A` and `B`) for X and Y movement.
- Prize coordinates for each claw machine.

### Output
- **Part One**: The fewest tokens needed to win as many prizes as possible with the original coordinates.
- **Part Two**: The fewest tokens needed to win as many prizes as possible after adding \(10^{13}\) to both X and Y prize coordinates.

### Approach
1. **Parsing Input**: Extract button configurations and prize coordinates using regular expressions.
2. **Part One**:
   - Brute force all possible combinations of button presses to match prize coordinates.
   - Calculate tokens required for valid button combinations.
3. **Part Two**:
   - Add \(10^{13}\) to prize coordinates.
   - Use symbolic solving for equations to find valid button combinations, minimizing computational cost.
4. Calculate the total tokens for all machines where prizes can be won.

### Part 1 Output:
```
Part 1 - Fewest tokens to win prizes: 32026
```

### Part 2 Output:
```
Part 2 - Fewest scaled tokens to win prizes: 89013607072065
```

## Conclusion
- **Part 1**: Demonstrated that a brute-force approach can determine the minimum tokens for the original prize coordinates.
- **Part 2**: Adjusted for scaled coordinates using symbolic equations, showing the method's flexibility and efficiency. The solution confirms the feasibility of winning prizes under drastically shifted conditions.
