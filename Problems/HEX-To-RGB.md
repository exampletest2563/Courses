# HEX to RGB Converter

## Problem Description
Given a hexadecimal color code, convert it to its equivalent RGB representation. The hexadecimal color code is a six-digit alphanumeric code representing red, green, and blue components of a color.

The conversion formula is as follows:
- The first two digits represent the red component.
- The next two digits represent the green component.
- The last two digits represent the blue component.

Each pair of digits is converted to its decimal equivalent.

## Input
The input will contain a single line representing the hexadecimal color code.

## Output
The output will contain a single line representing the RGB color code separated by commas.

## Constraints
- The input hexadecimal color code will be a six-digit alphanumeric string.
- Each character in the hexadecimal color code will be a digit (0-9) or a letter (A-F).

## Examples
|Input|Output|
|-|-|
|#FF0000|255,0,0|
|#00FF00|0,255,0|
|#0000FF|0,0,255|