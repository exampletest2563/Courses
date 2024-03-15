# 🔢 Enum

Sure! Here's an outline for the chapter on C# Enum:

### Chapter: C# Enum

#### Section 1: Introduction to Enums
- **1.1 What are Enums?**
  - Definition and purpose of Enums in C#
  - Explanation of how Enums help in representing a set of named constants

- **1.2 Enum Declaration Syntax**
  - Syntax for declaring Enums in C#
  - Naming conventions and best practices for Enum names

#### Section 2: Enum Basics
- **2.1 Enum Underlying Type**
  - Understanding the underlying data type associated with Enums
  - Explanation of default underlying types (integers) and customization options

- **2.2 Enum Values**
  - Defining Enum values and their corresponding integral values
  - Explanation of how Enum values are internally represented as integers

#### Section 3: Enumerations and Type Safety
- **3.1 Type Safety with Enums**
  - Benefits of using Enums for type safety in programming
  - Preventing invalid values with Enum types

- **3.2 Enum vs. Constants**
  - Comparison of Enums with traditional constant variables
  - Advantages of Enums over constants for representing a fixed set of values

#### Section 4: Working with Enums
- **4.1 Enum Methods and Properties**
  - Overview of built-in methods and properties provided by the Enum type
  - Usage examples of methods like `ToString()`, `Parse()`, `GetName()`, etc.

- **4.2 Enum Iteration**
  - Techniques for iterating through Enum values
  - Demonstrations of Enum iteration using `foreach` loops and LINQ queries

#### Section 5: Advanced Enum Features
- **5.1 Enum Attributes**
  - Introduction to Enum attributes for customizing Enum behavior
  - Usage examples of attributes like `Description`, `Flags`, etc.

- **5.2 Enum Flags**
  - Understanding Enum flags for representing bitwise combinations of Enum values
  - Usage scenarios and best practices for working with Enum flags

#### Section 6: Enum Conversions and Casting
- **6.1 Enum Conversions**
  - Implicit and explicit conversions between Enums and their underlying types
  - Techniques for converting Enum values to strings and vice versa

- **6.2 Enum Casting**
  - Casting Enum values to other data types and vice versa
  - Handling potential data loss and type compatibility issues

#### Section 7: Enum in Real-World Applications
- **7.1 Practical Examples**
  - Real-world scenarios where Enums are commonly used
  - Implementation examples in areas like user interfaces, configuration settings, error handling, etc.

- **7.2 Best Practices and Guidelines**
  - Best practices for designing Enum types and using them effectively in C# code
  - Guidelines for naming Enums, handling Enum changes, etc.

#### Section 8: Conclusion
- **8.1 Summary**
  - Recap of key concepts and features covered in the chapter
  - Importance of Enums in C# programming and their role in maintaining code clarity and correctness

- **8.2 Further Learning**
  - Resources and references for further exploration of Enum-related topics
  - Suggestions for additional reading and practical exercises to reinforce learning

### End of Chapter

## Enumerations

An `enum` (enumeration) in C# is a value type that defines a set of named integral constants.

Enumerations provide a more expressive and readable way to represent fixed sets of values, making code more self-documenting and maintainable.

An enumeration is declared using the `enum` keyword, followed by the enumeration name and a set of named constants enclosed in curly braces.

## Enumeration Declaration

Essentially, an `enum` is a type that only allows a set of finite options, and each option corresponds to a number. By default, those numbers are increasing in the order the values are declared, starting from zero.

An `enum` needs to be declared in a separate file.

```csharp
public enum DayOfWeek
{
	Monday,
	Tuesday,
	Wednesday,
	Thursday,
	Friday,
	Saturday,
	Sunday
}
```

// TODO: Sometimes, it's better to use `enum`, instead of boolean values, because of future functionality. The `bool status` variable will have only two possible values - true or false, while the `enum` has the possibility to add other values in the future, like `Deleted`, `NotFound`, etc.

```csharp
public enum Status
{
	Active,
	Inactive
}
```

An `enum` can derive from any of the following data types: `byte`, `sbyte`, `short`, `ushort`, `int`, `uint`, `long`, `ulong`. The default data type is `int`, and can be changed by specifying the type in the `enum` declaration.

```csharp
public enum Weekday : byte
{
	Monday = 1,
	Tuesday = 2,
	Wednesday = 3,
	Thursday = 4,
	Friday = 5
}
```

Constants in an `enum` are assigned default integer values starting from `0`. Custom values can be assigned explicitly, and subsequent constants continue from the last assigned value.

```csharp
public enum Month
{
	January = 1,
	February,
	March,
	April,
	May,
	June,
	July,
	August,
	September,
	October,
	November,
	December
}
```

## Use Cases & Benefits

Enumerations enhance code readability by providing meaningful names to integral constants, making the code more self-explanatory.

Instead of using "magic numbers" in the code, enumerations offer named constants, reducing the risk of errors and improving code maintainability.

```csharp
if (status == 0)
{
	// Code
}
else if (status == 1)
{
	// Code
}
```

```csharp
public enum OrderStatus
{
	Pending,
	Processing,
	Shipped,
	Delivered,
	Completed
}
```

```csharp
if (status == Status.Pending)
{
	// Code
}
else if (status == Status.Processing)
{
	// Code
}
```

```csharp
switch (day)
{
	case DayOfWeek.Saturday:
	case DayOfWeek.Sunday:
		Console.WriteLine("It's the weekend!");
		break;
	default:
		Console.WriteLine("It's a weekday.");
		break;
}
```

## The "Enum" Class

The `Enum` class in C# provides methods to retrieve the names and values of the constants defined in an `enum`.

```csharp
string[] dayNames = Enum.GetNames(typeof(DayOfWeek));
int[] dayValues = (int[])Enum.GetValues(typeof(DayOfWeek));
```

The `Enum` class allows parsing strings into `enum` values, providing a flexible way to convert user inputs.

```csharp
DayOfWeek parsedDay;

if (Enum.TryParse("Monday", out parsedDay))
{
	Console.WriteLine($"Parsed Day: {parsedDay}");
}
```