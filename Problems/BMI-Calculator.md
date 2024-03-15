# BMI Calculator
## Problem Description
Write a program that calculates the Body Mass Index (BMI) based on the user's weight (in kilograms) and height (in meters). The BMI is calculated using the formula:

\[ BMI = \frac{{weight}}{{height^2}} \]

Where:
- weight is the person's weight in kilograms.
- height is the person's height in meters.

The BMI is used to assess whether a person has a healthy body weight relative to their height. 

## Input
The input will contain two floating-point numbers separated by a space: the person's weight (in kilograms) and height (in meters), respectively.

## Output
The output will contain a single floating-point number: the calculated BMI.

## Constraints
- Both weight and height will be positive floating-point numbers.
- The weight will be in the range [10, 1000] kilograms.
- The height will be in the range [0.5, 3.0] meters.

## Examples
|Input|Output|
|-|-|
|65.5 1.75|21.39|
|75.0 1.80|23.15|
|55.2 1.60|21.56|