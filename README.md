# R Bug: mean() on Empty Vector

This repository demonstrates a common, yet easily overlooked, error in R when calculating the mean of an empty numeric vector. The `mean()` function throws a warning and returns `NaN` (Not a Number), potentially leading to unexpected behavior downstream in your code. The solution demonstrates a robust approach to handle such cases.

## Bug
The bug lies in directly applying the `mean()` function to an empty numeric vector.  This produces a warning and `NaN` as the result.

## Solution
The solution involves checking for an empty vector before calculating the mean. This can be done using a simple `if` condition.  If the vector is empty, you can return a default value (such as `0` or `NA`), preventing errors and ensuring your code functions correctly.  This makes the code robust and handles edge cases effectively.