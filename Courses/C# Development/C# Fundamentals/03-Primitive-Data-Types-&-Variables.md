# 🌱 Primitive Data Types & Variables

## Computer Memory (Computer Science)

## Data Types (Computer Science)

## Variables Introduction

Variables are containers for storing and managing data. They allow us to name and manipulate values.

```csharp
//          👇 Value
int number = 5;
//   👆 Variable name

Console.WriteLine(number); // 👈 Prints "5"
```

```csharp
//                   👇 Value
string firstName = "John";
//        👆 Variable name

Console.WriteLine(firstName); // 👈 Prints "John"
```

## Literals

C# supports binary and hexadecimal literals.

## Integer Data Types

Integers represent whole numbers without any decimal places.

C# provides several basic integer data types, including `byte`, `short`, `int`, and `long`. Each has its own range, allowing you to choose the right type based on the magnitude of the numbers you need to work with.

|Data Type|Bits|Byte(s)|Minimum Value|Maximum Value|
|-|-|-|-|-|
|sbyte|8|1|-128|127|
|byte|8|1|0|255|
|short|16|2|-32768|32767|
|ushort|16|2|0|65535|
|int|32|4|-2147483648|2147483647|
|uint|32|4|0|4294967295|
|long|64|8|-9223372036854775808|9223372036854775807|
|ulong|64|8|0|18446744073709551615|

Choosing the right integer type is about finding a balance between saving memory and accommodating the range of values our program needs.

The `byte` data type is the smallest integer type in C#. It can store values from `0` to `255`. Perfect for situations where memory is a precious resource!

The `short` data type provides a bit more range, accommodating values from `-32,768` to `32,767`. Useful when you need a bigger range than a byte but want to save memory compared to an int.

The `int` data type is our go-to for most integer needs. It can handle values from about `-2 billion` to `2 billion`.

When we arere dealing with astronomical numbers, we could use the `long` data type. It can hold values ranging from approximately `-9 quintillion` to `9 quintillion`.

## 🚢 Floating-Point Data Types

C# provides two basic floating-point data types - `float` and `double`.

Sometimes numbers get so large or small that scientific notation is more convenient. In C#, you can express floating-point literals using scientific notation, like `1.5e3` for 1500.

## 🤔 Precision, Accuracy & Computer Memory

Precision refers to how finely a value can be expressed, while accuracy relates to how closely the represented value matches the true value.

Floating-point numbers, like `float` and `double`, offer precision but with limitations. Due to binary representation, not all decimal fractions can be precisely represented. This can lead to rounding errors, impacting accuracy.

## 🚀 Decimal Precision Data Type

Unlike `float` and `double`, `decimal` is designed to represent decimal fractions with high precision.

Memory is a precious resource, and choosing the right data type involves trade-offs. While `float` and `double` are more memory-efficient, they sacrifice some precision. On the other hand, `decimal` provides precision but at the cost of increased memory usage.

In financial calculations, where precision is crucial, using the `decimal` type ensures accurate representation of monetary values, avoiding potential rounding discrepancies.

## 🌓 Boolean Data Type

Booleans represent `true` or `false` values.

```csharp
bool isWarm; // 👈 Default value: false
isWarm = true;

bool isSunny = true;
bool isRaining = false;
```

When a boolean variable is declared but not explicitly initialized, it defaults to `false`.

An expression that could be evaluated to `true` or `false` is called a `boolean` expression.

Imagine a smart home system. Using `boolean` values, we can represent whether lights are on or off, doors are locked or unlocked, and create smart rules based on these conditions.

Functions can return boolean values, indicating the success or failure of an operation. For example, a function to check if a user is authenticated might return `true` if authentication is successful.

## 🔣 Character Data Type

Characters represent individual symbols, letters, or digits.

```csharp
char symbol;
symbol = '$';

char letter = 'A';
char emoji = '😊';
```

Behind the scenes, characters in C# are represented using Unicode. Unicode allows the representation of a vast array of characters, including international symbols, emojis, and special characters.

## String Data Type

```csharp
string firstName = "John";
string lastName = "Smith";

Console.Write(firstName);
Console.Write(" "); // 👈 Represents a space (1 symbol)
Console.Write(lastName);
```

```csharp
string emptyString = ""; // 👈 0 symbols
Console.WriteLine(emptyString); // 👈 Prints ""
```

```csharp
string emptyString = string.Empty; // 👈 Special value
Console.WriteLine(emptyString); // 👈 Prints ""
```

## Variables Characteristics

## Variables Declaration & Initialization

Declaring a variable is like claiming a piece of memory and giving it a name.

```csharp
int age; // 👈 Variable Declaration
```

```csharp
age = 25; // 👈 Variable Initialization
```

```csharp
int age = 25; // 👈 Variable Declaration & Initialization
```

`Pseudocode`

```
<data_type> <variable_name> = <value>;
```

## 🏷️ Naming Variables

In C#, camelCase is the norm for naming variables. This means the first word is in lowercase, and subsequent words start with an uppercase letter. For instance, `totalAmount`, not `totalamount` or `TotalAmount`.

When naming variables, choose names that reflect the purpose or content of the data they hold. For example, instead of `x` or `y`, use names like `width` and `height` to convey the meaning of the variables.

|Data Type(s)|👌|👎|
|-|-|-|
|`byte`, `short`, `int`, `long`|`employeesCount`, `discountPercent`|`a`, `number`, `value`, `variable`|
|`float`, `double`, `decimal`|`productDiscount`||
|`boolean`|`isAuthenticated`, `isVisible`, `gameOver`||
|`char`|||
|`string`|`queryString`, `firstName`, `lastName`|`str`, `theStringThatHoldsFirstName`|

|Incorrect Variable Names|Reason|
|-|-|
|`a`, `i`, `x`|Too short|
|`iAmAVeryVeryVeryLongName`|Too long|
|`first_name`|Contains `_` (Snake case)|
|`2pac`|Starts with a number|
|`FIRSTNAME`|Uppercase|
|`FirstName`|Starts with a capital letter (Pascal case)|

Variables follow the Single Responsibility Principle. Each variable should have a clear and single responsibility. For instance, a variable named `userName` should store the user's name and nothing else.

## .NET Common Type System

|.NET Type|Alias|
|-|-|
|System.SByte|sbyte|
|System.Byte|byte|
|System.Int16|short|
|System.UInt16|ushort|
|System.Int32|int|
|System.UInt32|uint|
|System.Int64|long|
|System.UInt64|ulong|
|System.Single|float|
|System.Double|double|
|System.Decimal|decimal|
|System.Boolean|bool|
|System.Char|char|
|System.String|string|

## 📜 Guides

Aim for clarity and avoid using abbreviations or acronyms that may be unclear to others (or even yourself in the future!). Choose names that make your intentions obvious, promoting easy understanding.

It's okay to revisit and refine names as your code evolves. If you discover a more fitting name or if the purpose of a variable changes, take the time to refactor and keep your codebase tidy.

Follow a consistent naming style throughout your codebase. Consistency simplifies reading and understanding.

Sometimes we can use short names for our variables testing purposes - whether the solution will work or not. Once we find a suitable solution we can refactor the code.

Avoid using magic values (hard-coded values) without context. Instead, use named variables to give these values meaning.

Use `decimal` when handling monetary values, scientific measurements, or any scenario where exact representation of decimal fractions is essential.