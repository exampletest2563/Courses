# Password Validator
## Description
Write a program that checks if a sequence of characters represents a valid password.

A sequence of characters is considered a valid password if all of the following constraints are met:
- The length of the password should be in the following interval: **\[8..120]**;
- The password should contain at least one special character. Use the following ones: **@!#$**;
- The password should contain at least one digit: **\[0..9]**;
- The password should contain both lowercase and uppercase letters.
## Input
The input consists of a single value - a sequence of characters.
## Output
The output consists of a single value - **yes** or **no**.
## Examples
|Input|Output|
|-|-|
|234her@#ErgeT#!|yes|
|password123|no|
|qwerty|no|

# Password Validator
## Problem Description
You are tasked with creating a program that validates passwords based on certain criteria. A valid password must satisfy the following conditions:
- It must be at least 8 characters long.
- It must contain at least one uppercase letter.
- It must contain at least one lowercase letter.
- It must contain at least one digit.
- It may contain special characters.

Your program should take a password as input and determine whether it meets these criteria.

## Input
The input will contain a single line - the password string.

## Output
The output will contain a single line indicating whether the password is valid or not. If the password satisfies all the criteria, output "Valid password". Otherwise, output "Invalid password".

## Constraints
- The length of the password string will be at most 100 characters.

## Examples
|Input|Output|
|-|-|
|P@ssw0rd|Valid password|
|password123|Invalid password|
|StrongP@ssw0rd!|Valid password|
