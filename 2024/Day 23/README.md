# Day 23: LAN Party

## Problem Description

The Historians discover a map of a local network while at Easter Bunny HQ, with each line representing a connection between two computers. Connections are bidirectional. The goal is to:

1. Identify all sets of three computers where each computer is connected to the other two.
2. Narrow the results to sets where at least one computer's name starts with `t`.
3. Determine the largest fully connected group of computers (clique) in the network and use their names, sorted alphabetically and joined by commas, as the password for the LAN party.

## Solution Overview

### Part 1:
To identify all sets of three interconnected computers (triads), iterate through all possible combinations of computers in the network and validate if each is connected to the others. Further, filter these triads to include only those containing at least one computer with a name starting with `t`.

### Part 2:
To find the largest fully connected group of computers:
- Start with each computer as an independent group.
- Merge groups iteratively if a computer is connected to all members of another group.
- Identify the largest group and format their names alphabetically as the password.

### Input
A list of connections between computers, e.g.,
```
kh-tc
qp-kh
de-cg
ka-co
...
```
Each line represents a connection between two computers.

### Output
- Part 1: The count of triads containing at least one computer starting with `t`.
- Part 2: The password for the LAN party, derived from the largest fully connected group.

## Approach

1. **Parse Input:** Read the list of connections and build a dictionary mapping each computer to its directly connected neighbors.
2. **Find Triads:**
   - For each computer, check its connections to form potential triads.
   - Ensure all members of a triad are mutually connected.
   - Check if any computer in the triad starts with `t` and count these triads.
3. **Find Largest Clique:**
   - Treat each computer as its own group initially.
   - Merge groups iteratively based on mutual connectivity.
   - Extract the largest group and format their names alphabetically.

### Part 1 Output:
```
Part 1 - Number of three way connections with at least one 't' computer: 1110
```

### Part 2 Output:
```
Part 2 - Password to LAN party: ej,hm,ks,ms,ns,rb,rq,sc,so,un,vb,vd,wd
```

## Conclusion

### Part 1
The number of triads containing at least one computer starting with `t`.

### Part 2
The password for the LAN party, representing the largest fully connected group of computers.
