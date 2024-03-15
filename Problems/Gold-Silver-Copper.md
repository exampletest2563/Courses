# Gold, Silver, Copper
## Description
Write a program that converts copper coins to gold and silver coins.

**1 gold coin = 100 silver coins**

**1 silver coin = 100 copper coins**
## Input
The input consists of a single value - **C** (the amount of copper coins).
## Output
The output consists of three lines:
- On the first line - the gold coins amount in the following format: **{gold coins} gold**;
- On the second line - the silver coins amount in the following format: **{silver coins} silver**;
- On the third line - the remaining copper coins amount in the following format: **{copper coins} copper**;
## Examples
|Input|Output|
|-|-|
|23|0 gold<br />0 silver<br />23 copper|
|112|0 gold<br />1 silver<br />12 copper|
|543454|54 gold<br />34 silver<br />54 copper|

# Gold, Silver, Copper Calculation

## Problem Description
You are given a certain amount of money represented in terms of gold, silver, and copper. Your task is to calculate the total value in terms of the lowest currency unit (e.g., copper) considering the exchange rates between gold, silver, and copper.

The exchange rates are as follows:
- 1 gold = 100 silver
- 1 silver = 100 copper

For example, if you have 2 gold, 50 silver, and 25 copper, the total value would be calculated as follows:
- 2 gold = 2 * 100 * 100 = 20,000 copper
- 50 silver = 50 * 100 = 5,000 copper
- Total = 20,000 + 5,000 + 25 = 25,025 copper

## Input
The input will contain three integers separated by spaces, representing the amount of gold, silver, and copper, respectively.

## Output
The output will contain a single integer representing the total value in terms of copper.

## Constraints
- All amounts are non-negative integers.
- Each amount is less than 1,000.

## Examples
|Input|Output|
|-|-|
|2 50 25|25025|
|0 150 500|15500|
|10 0 0|1000000|