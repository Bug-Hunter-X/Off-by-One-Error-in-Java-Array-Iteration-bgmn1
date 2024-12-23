# Off-by-One Error in Java Array Iteration

This repository demonstrates a common off-by-one error in Java when iterating over arrays.  The `BuggyArray.java` file contains the erroneous code, while `FixedArray.java` provides the corrected version.  The error occurs due to incorrect loop bounds, attempting to access an array element beyond its valid index range.

## How to reproduce

1. Clone this repository.
2. Compile and run `BuggyArray.java`.  Observe the `ArrayIndexOutOfBoundsException`.
3. Compile and run `FixedArray.java`.  Observe the correct output.

## Analysis

The problem lies in the for loop condition `i <= arr.length`.  Java arrays are zero-indexed, meaning the valid indices range from 0 to `arr.length - 1`.  The loop should therefore use the condition `i < arr.length`. 