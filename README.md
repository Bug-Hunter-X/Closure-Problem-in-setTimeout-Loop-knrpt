# Closure Problem in setTimeout Loop

This repository demonstrates a common JavaScript closure problem that often arises when using `setTimeout` within a loop. The issue is that the value of `i` is not captured correctly within the closure created by `setTimeout`, leading to unexpected results.

## Bug Description

The code uses a `for` loop to schedule ten `setTimeout` calls. Each `setTimeout` function should print the value of `i` at the time it was scheduled.  However, due to the closure issue, all the `setTimeout` functions print the final value of `i` (10) after the loop completes.

## Solution

The solution uses an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, ensuring that the value of `i` is captured correctly at the time of each `setTimeout` call.