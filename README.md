# JavaScript Loose Comparison Unexpected Behavior with NaN and -0

This repository demonstrates an unusual behavior of JavaScript's loose comparison operator (`==`) when dealing with `NaN` (Not a Number) and `-0` (negative zero).

## The Bug

JavaScript's loose comparison (`==`) does not follow the usual rules of equality in certain cases.  Specifically:

* `NaN` is never equal to itself, even using loose comparison: `NaN == NaN` evaluates to `false`.
* `0` and `-0` are considered equal when using loose comparison: `0 == -0` evaluates to `true`.

The strict equality operator (`===`) correctly differentiates between `NaN` and `-0` from `0` and other numbers.

## The Solution

Always use strict equality (`===`) for comparisons in JavaScript.  This operator performs a type-safe comparison and avoids the unexpected results of loose comparison.