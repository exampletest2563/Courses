# HEX Color Validator
## Problem Description
Write a program that validates whether a given string is a valid **hexadecimal color code**.

The valid hexadecimal color code must satisfy the following conditions:
- It should start with the '#' symbol.
- It should be followed by the letters from a-f, A-F, and/or digits from 0-9.
- The length of the hexadecimal color code should be either 6 or 3, excluding the '#' symbol.
## Input
The input consists of a single value - a **string**.
## Output
The output consists of a single value - **true** or **false**.
## Examples
|Input|Output|
|-|-|
|`#abc`|true|
|`#000000`|true|
|`#FF0000`|true|
|`#12G56F`|false|

# HEX Color Validator

## Problem Description
You are given a list of strings, each representing a color in HEX format. Your task is to validate whether each color is a valid HEX color or not.

A valid HEX color must meet the following criteria:
- It must start with a '#' character.
- It must consist of either 3 or 6 characters following the '#' character.
- Each character must be a valid hexadecimal digit (0-9, A-F, a-f).

## Input
The input will contain a single line - a list of strings separated by spaces, each representing a color in HEX format.

## Output
The output will contain a single line. For each color in the input list, output "Valid" if it is a valid HEX color, and "Invalid" otherwise.

## Constraints
- The number of colors in the input list is at most 100.
- Each color string has a maximum length of 7 characters.

## Examples
|Input|Output|
|-|-|
|#FFF #ABC123 #000000|Valid Invalid Valid|
|#GGG #123456 #ABCDE|Invalid Valid Valid|