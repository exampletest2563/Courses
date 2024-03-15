# 📚 Text Processing

## String Trimming

```csharp
var firstName = Console.ReadLine();
var lastName = Console.ReadLine();

var fullName = firstName.Trim() + " " + lastName.Trim();
Console.WriteLine(fullName);
```

## String Casing

```csharp
var userInput = Console.ReadLine();

Console.WriteLine(userInput.ToLower());
Console.WriteLine(userInput.ToUpper());
```

```csharp
var userInput = Console.ReadLine().ToLower();
Console.WriteLine(userInput);
```

```csharp
var userInput = Console.ReadLine().ToUpper();
Console.WriteLine(userInput);
```

## String Concatenation

We can use `string.Join()` to concatenate array elements into a single string:

```csharp
char[] vowels = { 'a', 'e', 'i', 'o', 'u' };

// Joining and printing array elements
Console.WriteLine("Vowels: " + string.Join(", ", vowels));
```

Concatenating strings using a StringBuilder can offer performance advantages over simple string concatenation.

```csharp
StringBuilder stringBuilder = new StringBuilder();

for (int index = 1; index <= 100; index++)
{
	stringBuilder.Append(index);
	stringBuilder.Append(" ");
}

Console.WriteLine(stringBuilder.ToString());
```