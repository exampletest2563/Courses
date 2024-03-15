# Picture Dimensions - Portrait, Landscape or Square
## Problem Description
Given the dimensions (width and height) of a picture, determine whether it is a portrait, landscape, or square.

- If the width is greater than the height, the picture is landscape.
- If the height is greater than the width, the picture is portrait.
- If the width is equal to the height, the picture is square.

## Input
The input will contain two integers separated by a space representing the width and height of the picture.

## Output
The output will contain a single word indicating the type of the picture: "portrait", "landscape", or "square".

## Constraints
- 1 ≤ width, height ≤ 10^9

## Examples
|Input|Output|
|-|-|
|1920 1080|landscape|
|800 1200|portrait|
|1000 1000|square|