# Interest Calculation
## Problem Description
You are tasked with calculating the amount of money accumulated after a certain number of years based on an initial principal amount and an annual interest rate. The interest can be compounded annually, quarterly, monthly, or daily.

The formula for calculating the amount after compound interest is:

\[ A = P \times \left(1 + \frac{r}{n}\right)^{n \times t} \]

Where:
- \( A \) is the amount of money accumulated after \( t \) years.
- \( P \) is the principal amount (initial investment).
- \( r \) is the annual interest rate (expressed as a decimal).
- \( n \) is the number of times the interest is compounded per year.
- \( t \) is the number of years.

## Input
The input will contain three space-separated values:
1. \( P \) - the principal amount (a positive floating-point number).
2. \( r \) - the annual interest rate (a positive floating-point number representing a percentage).
3. \( n \) - the number of times the interest is compounded per year (an integer: 1, 4, 12, or 365).

## Output
The output will contain a single line:
- The accumulated amount of money after the specified number of years, rounded to two decimal places.

## Constraints
- \( 0 < P \)
- \( 0 < r < 100 \)
- \( n \) can be 1, 4, 12, or 365.
- \( 0 \leq t \leq 100 \)

## Examples
|Input|Output|
|-|-|
|1000 5.25 1|1103.63|
|5000 4.75 4|5724.60|
|2000 6.00 12|2413.27|