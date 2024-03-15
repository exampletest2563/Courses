# Data Storage

## Problem Description

White a program that takes the size of computer memory in gigabytes (GB) as input, calculates the equivalent size in megabytes (MB) and kilobytes (KB), and displays the results as output.

## Input

The input consists of a single value - an integer, representing the memory size in GB.

## Output

The output consists of a single line.

## Examples

|Input|Output|
|-|-|
|16|The memory size is 16 GB, which is equal to 16384 MB or 16777216 KB.|

# Data Storage - MB to GB
## Problem Description
Given a size in megabytes (MB), convert it to gigabytes (GB) and round the result to two decimal places.
## Input
The input will contain a single line with an integer representing the size in megabytes (MB).
## Output
The output will contain a single line with a floating-point number representing the size in gigabytes (GB), rounded to two decimal places.
## Constraints
- The input size will be a non-negative integer.
- The maximum value for the input size is \( 2^{31} - 1 \) (the maximum value representable by a 32-bit signed integer).
## Examples
|Input|Output|
|-|-|
|1024|1.00|
|1536|1.50|
|2048|2.00|