# 🔢 Enum

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