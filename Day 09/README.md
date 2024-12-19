# Day 9: Disk Fragmenter

## Problem Description

### Part One
The task is to help an amphipod compact files on a disk represented by a map of blocks. The disk map alternates between representing files and free space. The goal is to compact the disk by moving individual blocks of files to the leftmost available free space, then compute a checksum based on the final positions of the file blocks.

The disk map, such as `2333133121414131402`, represents a series of files and free spaces. Each number represents the length of a file or the length of free space, alternating between the two.

To calculate the checksum:
1. Move file blocks one at a time to the leftmost free space.
2. After the disk is compacted, calculate the checksum by summing the positions of blocks containing files, where each position is multiplied by the file ID.

### Part Two
The task is similar, but now the amphipod wants to move entire files rather than individual blocks. The goal is to move each file, in order of decreasing file ID, to the leftmost free space that can fit the file. If there is no space large enough, the file remains in place.

The checksum is calculated in the same way, based on the final positions of the file blocks after the files are moved.

## Solution Overview

### Input
The input is a single line representing the disk map as a series of numbers that alternate between file lengths and free space lengths.

### Output
The program outputs:
1. The checksum after compacting the disk by moving individual file blocks.
2. The checksum after compacting the disk by moving whole files.

### Approach
- **Part One**: Move file blocks one at a time into the leftmost available space and compute the checksum based on their final positions.
- **Part Two**: Move whole files into available spaces in order of decreasing file ID and compute the checksum similarly.

### Part 1 Output:
```
Part 1 - Sum of tight packing files:  6331212425418
```

### Part 2 Output:
```
Part 2 - Sum of loose packing files:  6363268339304
```

## Conclusion
- **Part 1**: We compacted the disk by moving individual file blocks and calculated the checksum based on their final positions.
- **Part 2**: We compacted the disk by moving whole files and computed the checksum after the files were rearranged.
