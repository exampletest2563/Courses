# 🧨 Exception Handling

## 🚫 Invalid Input

It is crucial to handle invalid input gracefully to prevent crashes and create user-friendly applications.

Different exceptions can occur based on the nature of invalid input. For example, `FormatException` is thrown when converting a string to a numeric type, and `OverflowException` can occur if the value is too large.

```csharp
Console.Write("Enter a number: ");
string userInput = Console.ReadLine();

if (int.TryParse(userInput, out int result))
{
	Console.WriteLine("You entered: {0}.", result);
}
else
{
	Console.WriteLine("Invalid input. Please enter a valid number.");
}
```

## Guides

Invalid input can come from various sources: typos, incorrect data types, or unexpected user behavior. Your program needs to be able to handle these scenarios without breaking. Always validate user input to ensure it meets your program's expectations.

Make error messages user-friendly! Instead of showing generic messages, provide context-specific feedback to guide users on how to correct their input.

// TODO: Invalid input! Please, enter a valid number.
// TODO: Something went wrong!

// TODO: Interface