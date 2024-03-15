# Quadratic Equation
## Description
Write a program that takes the coefficients of a quadratic equation (a, b, c) as input, calculates the roots of the equation using the quadratic formula, and displays the roots.
## Input
The input consists of a three numbers - **a**, **b** & **c**.
## Output
The output consists of a single line.
## Examples
|Input|Output|
|-|-|
|1<br />-3<br />2|The roots are: x = 2, x = 1.|
|2<br />4<br />2|There is only one root: x = -1.|
|1<br />2<br />2|There are no real roots.|

# Quadratic Equation
## Problem Description
Given a quadratic equation of the form \( ax^2 + bx + c = 0 \), where \( a \), \( b \), and \( c \) are real numbers, find the roots of the equation.

The roots of a quadratic equation can be calculated using the quadratic formula:

\[ x = \frac{{-b \pm \sqrt{{b^2 - 4ac}}}}{{2a}} \]

If the discriminant (\( b^2 - 4ac \)) is positive, the equation has two real roots. If the discriminant is zero, the equation has one real root. If the discriminant is negative, the equation has two complex roots.

## Input
The input will contain three space-separated real numbers: \( a \), \( b \), and \( c \) (|a|, |b|, |c| <= 1000).

## Output
The output will contain either:
- Two space-separated real numbers representing the two real roots of the equation, if the discriminant is positive.
- One real number representing the single real root of the equation, if the discriminant is zero.
- Two complex numbers in the form "a + bi" representing the two complex roots of the equation, if the discriminant is negative.

## Constraints
- \( |a|, |b|, |c| \) are real numbers such that |a|, |b|, |c| <= 1000.
- The equation will always have at least one real root.

## Examples
|Input|Output|
|-|-|
|1 -3 2|2 1|
|2 4 2|-1|
|1 2 5|-1 + 2i, -1 - 2i|