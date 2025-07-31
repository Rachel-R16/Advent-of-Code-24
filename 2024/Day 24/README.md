# Day 24: Crossed Wires

## Problem Description

You are tasked with debugging a monitoring device that uses boolean logic gates to process values and produce outputs. The device involves the following types of gates:

- **AND** gates output `1` if both inputs are `1`; otherwise, they output `0`.
- **OR** gates output `1` if at least one input is `1`; otherwise, they output `0`.
- **XOR** gates output `1` if the inputs are different; otherwise, they output `0`.

The system includes two sections in the input:
1. Initial values for certain wires.
2. Instructions that describe the gates and their connections.

The wires starting with `z` produce the final output, represented as a binary number. This binary number is then converted to a decimal value.

In Part Two, you discover that the system is designed to add two binary numbers represented by wires starting with `x` and `y`. However, the output wires of certain gates have been swapped, causing errors. Your goal is to identify and correct these swaps.

## Solution Overview

### Part 1
Simulate the system to resolve all wires' values, focusing on those starting with `z`. Combine the resolved values into a binary number, reverse it, and convert it to a decimal number.

### Part 2
Analyze the instructions to identify four pairs of gates whose outputs were swapped. Use the corrected configuration to ensure the system performs addition correctly. Output the sorted list of swapped wire names.

### Input

1. **Initial Values:**
   - Key-value pairs where keys are wire names (e.g., `x00`, `y01`) and values are integers (`0` or `1`).
   - Example:
     ```
     x00: 1
     y00: 0
     ```

2. **Gate Instructions:**
   - Operations connecting wires via gates.
   - Example:
     ```
     x00 AND y00 -> z00
     ```

### Output

1. **Part 1:** Decimal number produced by the system using wires starting with `z`.
2. **Part 2:** Sorted, comma-separated list of eight wires involved in swapped gate outputs.

### Approach

1. **Input Parsing:**
   - Separate initial values and gate instructions.
   - Store initial values in a dictionary and gate instructions as a list of tuples.

2. **Gate Simulation:**
   - Define a helper function to evaluate gates (`AND`, `OR`, `XOR`).
   - Iteratively resolve wires until all values are integers.

3. **Binary Conversion:**
   - Extract resolved values for `z` wires.
   - Form a binary string, reverse it, and convert to decimal.

4. **Error Detection (Part 2):**
   - Identify gates with swapped outputs by analyzing incorrect gate behaviors.
   - Collect and sort wire names involved in swaps.

### Part 1 Output:
```
Part 1 - Decimal number output on z: 61495910098126
```

### Part 2 Output:
```
Part 2 - Sorted eight wires involved in a swap: css,cwt,gdd,jmv,pqt,z05,z09,z37
```

## Conclusion

This challenge involved simulating a system of boolean logic gates and debugging incorrect configurations. Part 1 required resolving the system's outputs, while Part 2 focused on identifying and correcting swapped gates. These steps emphasized logical reasoning, system simulation, and error detection.

