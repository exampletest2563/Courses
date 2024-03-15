# Is Time To Eat?

## Problem Description
You are hungry and want to know if it's time to eat. Given the current time in the 24-hour format, determine if it's a suitable time for a meal. The meal times are categorized into Breakfast (06:00 - 09:59), Lunch (12:00 - 13:59), and Dinner (18:00 - 20:59).

## Input
The input will contain a single line representing the current time in the 24-hour format in the format "HH:MM", where HH represents the hour (00-23) and MM represents the minute (00-59).

## Output
The output will contain a single line indicating whether it's time to eat or not. If the time falls within the breakfast, lunch, or dinner time intervals, output "Time to Eat". Otherwise, output "Not Time to Eat".

## Constraints
- The input time will be in the format "HH:MM", where 00 <= HH <= 23 and 00 <= MM <= 59.

## Examples
|Input|Output|
|-|-|
|12:30|Time to Eat|
|07:45|Time to Eat|
|18:15|Time to Eat|