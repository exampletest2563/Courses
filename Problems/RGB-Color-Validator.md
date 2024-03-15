# RGB Color Validator
## Problem Description
Write a function to determine whether a given string represents a valid RGB color code. An RGB color code consists of three numbers (0-255) representing the red, green, and blue components of the color, respectively. The numbers are separated by commas and enclosed within parentheses. For example, "(255, 0, 128)" is a valid RGB color code.

## Input
The input will contain a single line - a string representing an RGB color code.

## Output
The output will contain a single line, indicating whether the input string represents a valid RGB color code. If the input is valid, output "Valid", otherwise output "Invalid".

## Constraints
- The input string will consist of characters '(', ')', ',', and digits '0'-'9'.
- The input string will have a length between 7 and 15 characters.

## Examples
|Input|Output|
|-|-|
|"(255,0,128)"|Valid|
|"(0, 128, 255)"|Valid|
|"(300, 128, 255)"|Invalid|