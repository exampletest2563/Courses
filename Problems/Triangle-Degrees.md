# Triangle Degrees

## Problem Description

Write a program that classifies the type of a triangle based on its angles.

## Input

The input consists of three numbers, representing the angles of a triangle:
- `side A`;
- `side B`;
- `side C`.

## Output

Display the classification of the triangle based on its angles:
- "Acute" for a triangle with all three angles less than 90 degrees.
- "Obtuse" for a triangle with one angle greater than 90 degrees.
- "Right" for a triangle with one angle equal to 90 degrees.

## Constraints

Your solution must comply with the following constraints:

- The sum of the three angles is always 180 degrees.

## Examples

|Input|Output|
|-|-|
|45<br />45<br />90|Right|
|60<br />70<br />50|Acute|

# Triangle Type By Degrees
## Problem Description
Given the three angles of a triangle in degrees, determine the type of triangle.

A triangle can be classified based on its angles as:
- Acute triangle: All three angles are less than 90 degrees.
- Right triangle: One angle is exactly 90 degrees.
- Obtuse triangle: One angle is greater than 90 degrees.

## Input
The input will contain three integers separated by spaces, representing the angles of the triangle in degrees.

## Output
The output will contain a single line indicating the type of triangle:
- "Acute" if all angles are less than 90 degrees.
- "Right" if one angle is exactly 90 degrees.
- "Obtuse" if one angle is greater than 90 degrees.

## Constraints
- 0 < Angle < 180
- The sum of the three angles will always be 180 degrees.

## Examples
|Input|Output|
|-|-|
|60 60 60|Acute|
|90 45 45|Right|
|100 40 40|Obtuse|