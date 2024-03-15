# 📝 Type Conversion & Casting

## ➡️ Type Conversion & Casting

Type conversion & casting are essential concepts in C# that allow you to convert data from one type to another.

Implicit Type Conversion, also known as widening or automatic conversion, occurs when C# automatically converts a smaller data type to a larger one without loss of data. It's like the language saying, "I've got this covered!"

Explicit Type Conversion, or casting, is required when converting a larger data type to a smaller one or when the conversion may result in data loss. It's the way of telling the compiler, "I know what I'm doing."

## Implicit Type Conversion

Implicit conversion occurs when there's no risk of losing data during the conversion. No need for extra syntax. For example, converting an `int` to a `long` or a `float` to a `double`.

```csharp
int intValue = 10;
long longValue = intValue;
 ```

Characters can be implicitly converted to numeric types.

```csharp
char firstLetter = 'A';
char secondLetter = firstLetter + 1;
Console.WriteLine(secondLetter);
```

## 🧮 Division By Zero

C# doesn't tolerate attempts to divide any non-zero numbers by zero in the context of integers numbers and throws a `System.DividedByZeroException`.

```csharp
int result = 10 / 0;
```

Division by zero leads to runtime errors, crashes, and unpredictable behavior.

In mathematics, division by zero is undefined because it leads to infinity or mathematical inconsistency. In programming, it's crucial to handle such cases to maintain the stability and reliability of your code.

## 🔄 Explicit Type Conversion

Explicit Type Conversion (Casting) is the deliberate conversion of a variable from one data type to another in C#. Unlike implicit conversion, this process requires explicit instructions from the developer.

Explicit conversion is necessary when we are dealing with scenarios that may involve data loss or when we want to be precise about how the conversion should occur.

```csharp
double doubleValue = 10.5;
int intValue = (int)doubleValue;
```

This informs C# to convert the floating-point value to an integer explicitly. It is necessary because casting from a floating-point type to an integer may result in data loss.

```csharp
double quotient = 7 / 2;
Console.WriteLine(quotient);
```

```csharp
double quotient = 7 / 2; // This will not convert the result to double, because the expression itself is evaluated to int
Console.WriteLine(quotient);
```

```csharp
double quotient = 7 / 2.0; // 2f, 2F, 2d, 2D, 2m, 2M, (float)2, (double)2, (decimal)2
Console.WriteLine(quotient);
```

Explicit Type Conversion may lead to data loss.

Common explicit conversions include converting between numeric types, such as `int` to `double` or `float` to `int`. Additionally, converting from `string` to numeric types is a common scenario.

Explicit conversion may lead to data loss or unexpected results if the target type can't accommodate the full range of values from the source type.

## 🧨 Overflow Exceptions

Overflow exceptions occur when a numeric operation results in a value that exceeds the limits of the data type.

```csharp
double number = double.MaxValue;

Console.WriteLine(number + 1);
```

```csharp
double number = double.MinValue;

Console.WriteLine(number - 1);
```

```csharp
long bigNumber = 1000000000000;

int smallNumber = (int)bigNumber;

Console.WriteLine(smallNumber);
```

Overflow can lead to unpredictable behavior, incorrect results, and, in the worst cases, crashes. It's crucial to understand how to detect and handle overflow scenarios to ensure the stability of your code.

If we have two large `int` values, say `int.MaxValue = 2,147,483,647` and we attempt to add them together, it will result in an overflow exception. C# won't silently accept the overflow; it will throw a `System.OverflowException`.

Overflow isn't exclusive to integers. It can happen with other numeric types like `long`, `float`, and `double`. Understanding the limits of each type is crucial to avoiding unexpected results.

```csharp
int maxInt = Int.MaxValue;
```

## 🖨️ Conversion To String

Conversion to string is the process of transforming data in their textual representation.

```csharp
int age = 25;
Console.WriteLine(age.ToString());
```

```csharp
double pi = 3.14159;
Console.WriteLine(pi.ToString());
```

## The "Convert" Class

The `Convert` class in C# provides methods for converting between various data types.

```csharp
string text = "23";
int number = Convert.ToInt32(text);

Console.WriteLine(text + 2); // 232
Console.WriteLine(number + 2); // 25
```

```csharp
double price = 29.99;
Console.WriteLine(Convert.ToInt32(price));
```

## Parsing Data

In the real world, data often comes in the form of strings, whether from user input, external files, or network communications. Parsing allows you to convert these strings into usable data within our program.

```csharp
string text = "23";
int number = int.Parse(text);

Console.WriteLine(text + 2); // 232
Console.WriteLine(number + 2); // 25
```

Be cautious with invalid input! If you attempt to parse a non-numeric string like `Hello`, it will throw a `System.FormatException`.

## Type Inference

C# is a statically typed language, but it also supports type inference. The `var` keyword allows the compiler to determine the data type automatically.

```csharp
var greeting = "Hello World"; // Type string

var expression = 12 * (2 + 3); // Type int
```

## 📜 Guides

By incorporating additional logic before performing the division, we can ensure that the denominator is non-zero. If it is, proceed with the division; otherwise, take appropriate action.

It's crucial to handle scenarios where explicit conversion may not be valid. For example, attempting to convert a `string` that doesn't represent a valid numeric value to an `int` could result in an exception. Use techniques like `int.TryParse` for safer conversions.