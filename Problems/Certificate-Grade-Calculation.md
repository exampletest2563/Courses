# Certificate Grade Calculation
## Problem Description
You are tasked with calculating the final grade for a certificate based on the scores obtained in various subjects. The final grade is determined by the average score obtained across all subjects. The grading scale is as follows:
- A: 90 or above
- B: 80 - 89
- C: 70 - 79
- D: 60 - 69
- F: Below 60

The final grade is determined by rounding the average score to the nearest integer.

## Input
The input will contain multiple lines, each representing a subject score. Each line will consist of two space-separated values: the subject name (a string) and the score (an integer between 0 and 100).

## Output
The output will contain a single line representing the final grade obtained.

## Constraints
- The number of subjects will be between 1 and 10.
- Each subject score will be between 0 and 100.

## Examples
|Input|Output|
|-|-|
|Math 85<br>Science 75<br>History 90|B|
|Physics 95<br>Chemistry 82<br>Biology 88|A|
|Literature 60<br>Art 72<br>Music 55|C|