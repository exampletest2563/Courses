# Guess The Number

## Problem Description
You are playing a game where you need to guess a secret number. The secret number is randomly generated between a given range. You have a limited number of attempts to guess the correct number. After each guess, you will receive feedback indicating whether your guess is too low, too high, or correct.

## Input
The input will contain two integers, **N** and **K**, separated by a space, where **N** represents the range of numbers (from 1 to **N**) within which the secret number is generated, and **K** represents the number of attempts you have to guess the correct number.

## Output
The output will contain a single line indicating the result of your guess:
- If your guess is correct, output "Correct!"
- If your guess is too low, output "Too low! Try again."
- If your guess is too high, output "Too high! Try again."

## Constraints
- 1 ≤ **N** ≤ 1000
- 1 ≤ **K** ≤ 100

## Examples
|Input|Output|
|-|-|
|10 3|Too low! Try again.|
|5 2|Too high! Try again.|
|8 4|Correct!|