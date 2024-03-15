# Generate Password By Constraints

## Problem Description
You are tasked with generating a password based on given constraints. The password must satisfy specific criteria such as length, inclusion of uppercase and lowercase letters, numbers, and special characters.

## Input
The input will contain a single line specifying the constraints for generating the password.

## Output
The output will contain a single line representing the generated password.

## Constraints
- The length of the password (n) will be between 8 and 20 characters.
- The password must contain at least one uppercase letter, one lowercase letter, one digit, and one special character.
- The special characters allowed are: !@#$%^&*()_+[]{}|;':,.<>?/
- No spaces are allowed in the password.

## Examples
| Input         | Output       |
|---------------|--------------|
| length=12     | P@ssw0rd123! |
| length=10     | Secret@123   |
| length=15     | MyP@ssw0rd!123 |