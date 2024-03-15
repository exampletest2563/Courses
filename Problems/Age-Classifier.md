# Age Classifier

## Problem Description
Create a program that classifies a person's age based on the following criteria:
- If the age is 0-2 years inclusive, classify as "Infant".
- If the age is 3-12 years inclusive, classify as "Child".
- If the age is 13-19 years inclusive, classify as "Teenager".
- If the age is 20 or older, classify as "Adult".

## Input
The input will contain a single integer - the person's age.

## Output
The output will contain a single line specifying the classification of the person's age.

## Constraints
- Age will be a non-negative integer.
- Age will not exceed 150.

## Examples
|Input|Output|
|-|-|
|1|Infant|
|10|Child|
|16|Teenager|