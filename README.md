# Unexpected NaN Comparison in JavaScript

This repository demonstrates a common, yet subtle, error in JavaScript related to comparing NaN (Not a Number) values.  JavaScript's loose comparison (==) and strict comparison (===) operators behave unexpectedly when dealing with NaN.

The `bug.js` file showcases the unexpected result: `NaN === NaN` evaluates to `false`.  This is counterintuitive since NaN represents an undefined or unrepresentable numerical value.

The `bugSolution.js` file provides a solution using the `Number.isNaN()` function, which correctly identifies NaN values.

## How to reproduce

1. Clone this repository.
2. Run `node bug.js` to observe the unexpected behavior.
3. Run `node bugSolution.js` to see the corrected solution using `Number.isNaN()`.

## Lesson Learned

Always use `Number.isNaN()` to reliably check for NaN values.  Avoid using loose or strict equality comparisons directly with NaN.