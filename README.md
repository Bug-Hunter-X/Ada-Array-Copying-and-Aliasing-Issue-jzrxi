# Ada Array Copying and Aliasing Bug

This repository demonstrates a common but subtle bug in Ada related to array copying.  In Ada, assigning one array to another doesn't create a distinct copy; instead, it creates an alias.  Modifying the 'copy' consequently affects the original array.

The `bug.ada` file shows the problematic code. The `bugSolution.ada` shows the corrected version using explicit copying.

## How to Reproduce

1. Compile and run `bug.ada`. Observe that the output shows the original array `A` modified even though only `B` was explicitly changed.
2. Compile and run `bugSolution.ada`. This version correctly copies the array, resulting in `A` remaining unchanged.