# Equal Elements (As Sets)

## Problem Description
Given an array of integers, determine if all elements in the array are equal when treated as sets, i.e., if all elements are the same when duplicates are removed.

For example, in the array `[1, 2, 2, 1, 3]`, when treated as a set, it becomes `{1, 2, 3}`, and since all elements are equal, the output is `true`. However, in the array `[1, 2, 3, 4, 5]`, when treated as a set, it becomes `{1, 2, 3, 4, 5}`, and since not all elements are equal, the output is `false`.

## Input
The input will contain a single line representing the array of integers separated by spaces.

## Output
The output will contain a single line representing whether all elements in the array are equal when treated as sets. Output `true` if all elements are equal, and `false` otherwise.

## Constraints
- The length of the array (N) will be at most 1000.
- Each element of the array will be an integer in the range [-10^6, 10^6].

## Examples
|Input|Output|
|-|-|
|1 2 2 1 3|true|
|1 2 3 4 5|false|