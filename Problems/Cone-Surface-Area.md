# Cone Surface Area
## Problem Description
You are tasked with finding the surface area of a cone given its radius and slant height. The surface area of a cone consists of the lateral surface area and the base area.

The lateral surface area (A) of a cone can be calculated using the formula:

\[ A = \pi \times r \times l \]

where:
- \( r \) is the radius of the cone's base,
- \( l \) is the slant height of the cone.

The base area (B) of a cone can be calculated using the formula for the area of a circle:

\[ B = \pi \times r^2 \]

The total surface area (T) of a cone is the sum of its lateral surface area and its base area:

\[ T = A + B \]

## Input
The input will contain three floating-point numbers separated by spaces:
1. The radius of the cone's base (r), where \( 0 < r \leq 10^9 \).
2. The slant height of the cone (l), where \( 0 < l \leq 10^9 \).
3. The height of the cone (h), where \( 0 < h \leq 10^9 \).

## Output
The output will contain a single floating-point number rounded to two decimal places, representing the total surface area of the cone.

## Constraints
- All input values are positive floating-point numbers.
- The output should be rounded to two decimal places.

## Examples
|Input|Output|
|-|-|
|3.5 4.2 5.0|83.95|
|1.0 3.0 4.0|37.70|
|2.5 6.0 7.5|141.38|