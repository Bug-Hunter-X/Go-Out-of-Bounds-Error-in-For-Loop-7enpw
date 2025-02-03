# Go Out of Bounds Error in For Loop

This example demonstrates a common error in Go: an out-of-bounds array access within a `for` loop. The incorrect loop condition `i <= len(a)` leads to a runtime panic.  The solution shows the correct loop condition `i < len(a)`.

## Bug

The `bug.go` file contains a function that iterates over an integer slice, attempting to print each element.  Due to an off-by-one error in the loop condition, it attempts to access an element beyond the array bounds, resulting in a runtime panic.

## Solution

The `bugSolution.go` file provides the corrected function. The loop condition is changed to `i < len(a)`, ensuring that the loop terminates before accessing any out-of-bounds elements.