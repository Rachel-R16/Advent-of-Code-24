# Day 17: Chronospatial Computer

## Problem Description
The problem involves simulating a 3-bit computer's program with three registers (A, B, and C) and executing various instructions to produce an output. The input consists of the initial values of registers and a program consisting of opcodes and operands.

### Part One
You need to determine the output produced by the program when initialized with given register values. The program will halt once all instructions are processed. Your task is to collect and print the values produced by the `out` instructions, joined by commas.

### Part Two
The program is supposed to output a copy of itself, but the value of register A has been corrupted. The task is to find the smallest initial value for register A that causes the program to output an exact copy of itself.

## Solution Overview

### Input
The input consists of:
1. Three lines representing the initial values of registers A, B, and C.
2. A line containing the program, which consists of opcodes and operands.

### Output
For Part 1, the output is a series of values produced by the `out` instructions in the program. These values are joined by commas.

For Part 2, the output is the smallest initial value for register A that causes the program to output an exact copy of itself.

### Approach
1. Parse the input to extract the initial register values and program.
2. Implement the program simulation:
   - Use a loop to process each instruction in the program, updating the registers accordingly.
   - Handle the various opcodes (`adv`, `bxl`, `bst`, `jnz`, `bxc`, `out`, `bdv`, `cdv`).
   - Collect the output produced by the `out` instructions.
3. For Part 2, iterate over possible values for register A and find the value that produces the program's output as a copy of the program itself.

### Part 1 Output:
```
Part 1 - Output values: 3,5,0,1,5,1,5,1,0
```

### Part 2 Output:
```
Part 2 - Optimal value for register A: 107413700225434
```

## Conclusion
This solution simulates the behavior of a 3-bit computer, processes the program instructions, and solves both parts of the puzzle by simulating the program and finding the required output.
