### Problem Description: Month Printer

Write a function that takes the month and year as input and prints the calendar for that month in a format similar to the output of the UNIX cal command. The function should prompt the user to enter the month and year, and then print out the calendar for the specified month and year.

#### Function Signature

python

`def print_month_calendar(month: int, year: int) -> None:     pass`

#### Example

python

`print_month_calendar(3, 2023) # Output: # March 2023 # Su Mo Tu We Th Fr Sa #                 1  2  3  4 #  5  6  7  8  9 10 11 # 12 13 14 15 16 17 18 # 19 20 21 22 23 24 25 # 26 27 28 29 30 31`

#### Constraints

- The input `month` is an integer between 1 and 12, and `year` is a valid year.

This function will allow users to input a specific month and year, and then display the calendar for that month and year in a clear and organized format.

# Print & Format All Days From Current Month (as a Calendar)

## Problem Description
You are tasked with writing a program that prints and formats all the days from the current month as a calendar. The calendar should display the days of the week and align them in a visually appealing format.

## Input
The input will not be required for this problem.

## Output
The output will be the formatted calendar for the current month.

## Constraints
- The program should display the calendar for the current month only.
- The calendar should be properly formatted with days of the week aligned.

## Examples
|Input|Output|
|-|-|
|N/A|```
      March 2024
   -----------------
   Sun Mon Tue Wed Thu Fri Sat
   -----------------
                  1   2   3
    4   5   6   7   8   9  10
   11  12  13  14  15  16  17
   18  19  20  21  22  23  24
   25  26  27  28  29  30  31
   ```|
|N/A|```
      April 2024
   -----------------
   Sun Mon Tue Wed Thu Fri Sat
   -----------------
          1   2   3   4   5   6
    7   8   9  10  11  12  13
   14  15  16  17  18  19  20
   21  22  23  24  25  26  27
   28  29  30
   ```|