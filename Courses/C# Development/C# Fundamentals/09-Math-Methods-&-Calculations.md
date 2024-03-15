# 📐 Math Methods & Calculations

## 🔢 The "Math" Class

The `Math` class provides constants and methods for trigonometric, logarithmic, and other common mathematical functions.

Some of the functions offered by the `Math` class include:
- `Math.Abs(x)`: Returns the absolute value of `x`;
- `Math.Sqrt(x)`: Returns the square root of `x`;
- `Math.Pow(x, y)`: Returns `x` raised to the power of `y`;
- `Math.Round(x)`: Rounds `x` to the nearest integer.

The `Math` class also provides useful constants:
- `Math.PI`: The mathematical constant `π`;
- `Math.E`: The mathematical constant `e`.

## 📈 The "Max" Method

The `Math.Max` method returns the larger of two given numbers.

```csharp
var firstNumber = int.Parse(Console.ReadLine());
var secondNumber = int.Parse(Console.ReadLine());

//                   👇 Evaluated at runtime
var maxNumber = Math.Max(firstNumber, secondNumber);
Console.WriteLine(maxNumber);
```

```csharp
var firstNumber = int.Parse(Console.ReadLine());
var secondNumber = int.Parse(Console.ReadLine());

var maxNumber = 0;

//             👇 We could use ">" too
if (firstNumber >= secondNumber)
{
	maxNumber = firstNumber;
}
else
{
	maxNumber = secondNumber;
}

Console.WriteLine(maxNumber);
```

```csharp
var firstNumber = int.Parse(Console.ReadLine());
var secondNumber = int.Parse(Console.ReadLine());

//                         👇 We could use ">" too
var maxNumber = firstNumber >= secondNumber ? firstNumber : secondNumber;
Console.WriteLine(maxNumber);
```

## 📉 The "Min" Method

The `Math.Min` method returns the smaller of two given numbers.

```csharp
var firstNumber = int.Parse(Console.ReadLine());
var secondNumber = int.Parse(Console.ReadLine());

//                   👇 Evaluated at runtime
var minNumber = Math.Min(firstNumber, secondNumber);
Console.WriteLine(minNumber);
```

```csharp
var firstNumber = int.Parse(Console.ReadLine());
var secondNumber = int.Parse(Console.ReadLine());

var minNumber = 0;

//             👇 We could use "<" too
if (firstNumber <= secondNumber)
{
	minNumber = firstNumber;
}
else
{
	minNumber = secondNumber;
}

Console.WriteLine(minNumber);
```

```csharp
var firstNumber = int.Parse(Console.ReadLine());
var secondNumber = int.Parse(Console.ReadLine());

//                         👇 We could use "<" too
var minNumber = firstNumber <= secondNumber ? firstNumber : secondNumber;
Console.WriteLine(minNumber);
```

## 📏 Absolute Value

In mathematics, the absolute value or modulus of a real number is the non-negative value of the number without regard to its sign.

It is denoted by `|x|`, where `x` is a real number.

The `Math.Abs` method returns the non-negative value of `x`.

```csharp
var x = int.Parse(Console.ReadLine());

var absoluteValue = Math.Abs(x);
Console.WriteLine(absoluteValue);
```

The absolute value of a number measures the distance of the number from zero along the real number line, regardless of its direction, and is always a positive value.

Normally, we would use such functions when working with the value itself, regardless of its sign.

```csharp
var x = int.Parse(Console.ReadLine()); // Example: "-5"

//                               👇 -(-5) = 5
var absoluteValue = x >= 0 ? x : -x;
Console.WriteLine(absoluteValue); // 👈 Prints "5"
```

## ✨ Exponentiation

In mathematics, exponentiation is the process of raising a number to a specific power.

The `Math.Pow` method returns a specified number raised to the specified power.

```csharp
var baseNumber = int.Parse(Console.ReadLine()); // Example: "2"
var exponent = int.Parse(Console.ReadLine()); // Example: "5"

var result = Math.Pow(baseNumber, exponent);
Console.WriteLine(result); // 👈 Prints "32"
```

```csharp
var number = int.Parse(Console.ReadLine()); // Example: "2"
var power = int.Parse(Console.ReadLine()); // Example: "5"
var result = 1;

for (int counter = 1; counter <= power; counter++)
{
	result *= number;
}

Console.WriteLine(result); // 👈 Prints "32"
```

The `Math.Pow` method can handle negative exponents, resulting in fractions or decimals.

## 🌱 Square Root

In mathematics, the square root of a number is a value that, when multiplied by itself, gives the original number.

The `Math.Sqrt` method returns the square root of a specified number.

```csharp
var number = int.Parse(Console.ReadLine()); // Example: "9"

var squareRoot = Math.Sqrt(number);
Console.WriteLine(squareRoot); // 👈 Prints "3"
```

While square roots of negative numbers are not real in the realm of real numbers, C# handles them using the `NaN` (Not a Number) value.

```csharp
var number = -4;

var squareRoot = Math.Sqrt(number);
Console.WriteLine(squareRoot); // 👈 Prints "NaN"
```

## 🎯 Rounding Numbers

Rounding could be used to present numbers in a more manageable form, especially when dealing with real-world scenarios that require precision.

The `Math.Floor` method returns the largest integral value less than or equal to the specified number.

```csharp
var realNumber = double.Parse(Console.ReadLine()); // Example: "7.64"

var roundedValue = Math.Floor(realNumber);
Console.WriteLine(roundedValue); // 👈 Prints "7"
```

The `Math.Ceiling` method returns the smallest integral value that is greater than or equal to the specified number.

```csharp
var realNumber = double.Parse(Console.ReadLine()); // Example: "7.24

var roundedValue = Math.Ceiling(realNumber);
Console.WriteLine(roundedValue); // 👈 Prints "8"
```

The `Math.Round` method rounds a decimal value to a specified number of fractional digits using the specified rounding convention.

```csharp
var realNumber = double.Parse(Console.ReadLine());

// 2 👈 Number of fractional digits
// MidpointRounding.AwayFromZero 👈 Rounding convention
var roundedNumber = Math.Round(realNumber, 2, MidpointRounding.AwayFromZero);

Console.WriteLine(roundedNumber);
```

The `Math.Round` method supports two rounding conventions for handling midpoint values:
- Rounding away from zero: This form of rounding is represented by `MidpointRounding.AwayFromZero`;
- Rounding to nearest even, or banker's rounding: This form of rounding is represented by `MidpointRounding.ToEven`.

The `Math.Truncate` method returns the number that remains after any fractional digits have been discarded.

```csharp
var realNumber = double.Parse(Console.ReadLine()); // Example: "6.8"

var doubleNumber = Math.Truncate(realNumber); // 👈 Data Type: System.Double
Console.WriteLine(doubleNumber); // 👈 Prints "6"
```

```csharp
var realNumber = double.Parse(Console.ReadLine()); // Example: "6.8"

var integerNumber = (int)(realNumber); // 👈 Data Type: System.Int32
Console.WriteLine(integerNumber); // 👈 Prints "6"
```