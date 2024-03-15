# Discount Calculation
## Problem Description
You are required to implement a discount calculation program for a shopping cart. Given the total price of items in the cart and the discount rate, calculate the final price after applying the discount.

## Input
The input will contain two space-separated integers: `total_price` and `discount_rate`, where `total_price` (0 <= total_price <= 100000) represents the total price of items in the cart and `discount_rate` (0 <= discount_rate <= 100) represents the discount rate as a percentage.

## Output
The output will contain a single floating-point number representing the final price after applying the discount. The final price should be rounded to two decimal places.

## Constraints
- 0 <= total_price <= 100000 (total price of items)
- 0 <= discount_rate <= 100 (discount rate in percentage)

## Examples
|Input|Output|
|-|-|
|100 10|90.00|
|50 20|40.00|
|200 15|170.00|