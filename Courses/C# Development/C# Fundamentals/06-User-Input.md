# ✍️ User Input

## 🔁 I/O Operations

## ✍️ Reading User Input

In C#, the `Console` class provides a streamlined mechanism for interacting with the standard input (`Console.In`) and output (`Console.Out`) streams.

```csharp
Console.Write("Enter your name: ");

string username = Console.ReadLine(); // 👈 Example: "John"

Console.WriteLine("Hello, " + username + "!"); // 👈 Prints: "Hello, John!"
```

The `Console.ReadLine` method reads a line of text entered by the user and returns it as a string.

```csharp
string firstNumber = Console.ReadLine(); // Example: "2"
string secondNumber = Console.ReadLine(); // Example: "3"

Console.WriteLine(firstNumber + secondNumber); // Prints: "23"
```

In order to convert a string to an integer, we can use the `Int32.Parse` method.

```csharp
Console.Write("Enter your age: ");

string userInput = Console.ReadLine(); // 👈 Example: "34"
int userAge = Int32.Parse(userInput); // 👈 Converts "34" to 34

Console.WriteLine(userAge + 10); // 👈 Prints: "44"
```

`Int32` and `int` are aliases.

```csharp
Console.Write("Enter your age: ");

string userInput = Console.ReadLine();
int userAge = int.Parse(userInput);

Console.WriteLine(userAge);
```

We can omit the declaration of the `userInput` variable:

```csharp
Console.Write("Enter your age: ");

int userAge = int.Parse(Console.ReadLine());

Console.WriteLine(userAge);
```

```csharp
Console.Write("Enter your age: ");

int userAge = Convert.ToInt32(Console.ReadLine());

Console.WriteLine(userAge);
```

## 🚫 Invalid Input

## 🗝️ Key Events

Sometimes, we want a capture a single keypress instead of a whole line. The `Console.ReadKey` method allows capturing key events.

```csharp
ConsoleKeyInfo keyInfo = Console.ReadKey();
Console.WriteLine("Key pressed: " + keyInfo.KeyChar);
```

In order to check if the user pressed the \[Enter\] key, we can use the `ConsoleKey` enumeration. It includes a variety of keys, from letters and numbers to function keys and modifiers.

```csharp
ConsoleKeyInfo keyInfo = Console.ReadKey();

if (keyInfo.Key == ConsoleKey.Enter)
{
    Console.WriteLine("Enter key pressed!");
}
```

The `Console.ReadKey` method could be used to detect special keys and modifiers, too. Modifiers are accessible via the `ConsoleModifiers` enumeration.

```csharp
ConsoleKeyInfo keyInfo = Console.ReadKey();

if (keyInfo.Key == ConsoleKey.A && keyInfo.Modifiers == ConsoleModifiers.Shift)
{
    Console.WriteLine("[Shift] + [A] pressed!");
}
```

## 📜 Guides