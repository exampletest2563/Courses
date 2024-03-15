# Next N Leap Years

## Problem Description
You are tasked with writing a program that generates the next N leap years after a given year. A leap year is a year that is evenly divisible by 4 but not by 100 unless it is also divisible by 400. For example, 2000 and 2400 are leap years, while 1800, 1900, and 2100 are not.

## Input
The input will contain a single integer N representing the number of leap years to generate, followed by an integer year representing the starting year.

## Output
The output will contain N lines, each containing a leap year in ascending order starting from the year following the input year.

## Constraints
- 1 ≤ N ≤ 100
- 1 ≤ year ≤ 10^4

## Examples
|Input|Output|
|-|-|
|5 2022|2024<br>2028<br>2032<br>2036<br>2040|
|3 2100|2104<br>2108<br>2112|