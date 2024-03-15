# 🔃 Control Flow - Loops

## 🔁 Repetitive Actions

Often, we encounter scenarios where a certain action needs to be performed multiple times.

```csharp
var pagesCount = 273;

for (int pageCounter = 1; pageCounter <= pagesCount; pageCounter++)
{
	// Read One Page...
}
```

```csharp
var success = false;

while (!success)
{
	// Don't Give Up
	// Try Again
}
```

Loops are used to automate repetitive tasks.

## For Loop

The `for` loop consists of four main components:
- `Initialization`: Initializes a new local variable that can only be used within the loop;
- `Condition`: The loop only runs when the condition is true;
- `Code Block`: The block of code inside the loop that gets repeated;
- `Iteration Update`: How the variable changes every time the loop runs.

`Pseudocode`

```csharp
for (initialization; condition; update)
{
	// Code
}
```

```csharp
for (int counter = 1; counter <= 10; counter++)
{
	Console.WriteLine("Iteration: " + counter);
}
```

```csharp
for (int counter = 10; counter >= 0; counter--)
{
	Console.WriteLine(counter);
}
```

## While Loop

The `while` loop consists of a single condition that determines whether the loop should continue or break. The `while` loop repeats as long as a specified condition is true.

`Pseudocode`

```csharp
while (condition)
{
	// Code
}
```

```csharp
var counter = 1;

while (counter <= 10)
{
	Console.WriteLine("Iteration: " + counter);
	counter++;
}
```

The `while` loop consists of three main components:
- `Condition`: The loop only runs when the condition is true;
- `Code Block`: The block of code inside the loop that gets repeated;
- `Iteration Update`: A statement that updates values used in the loop condition.

## Do-While Loop

The `do-while` loop guarantees at least one execution, as it evaluates the condition after the first iteration.

`Pseudocode`

```csharp
do
{
	// Code
} while (condition);
```

```csharp
int age;

do
{
	age = int.Parse(Console.ReadLine());
	Console.WriteLine(age);
} while (age < 0 || 100 < age);
```

## Infinite Loops

Be cautious with infinite loops. Infinite loops are loops without a defined exit condition (or a condition that is not updated properly or as expected). Make sure there's a clear exit condition to avoid unintentional infinite repetition.

## ⛔ The "break" Keyword

The `break` keyword allows us to exit a loop before its natural completion, based on a certain condition.

```csharp
for (int counter = 1; counter <= 10; counter++)
{
	if (counter == 5)
	{
		break;
	}
	
	Console.WriteLine("Iteration: " + counter);
}
```

## ⏭️ The "continue" Keyword

The `continue` keyword allows us to skip the rest of the current iteration and move to the next one.

```csharp
for (int counter = 1; counter <= 10; counter++)
{
	if (counter % 2 == 0)
	{
		continue;
	}
	
	Console.WriteLine("Iteration: " + counter);
}
```

## Nested Loops

Nesting involves placing one loop inside the body of another.

```csharp
for (int row = 1; row <= 3; row++)
{
	for (int column = 1; column <= 3; column++)
	{
		Console.Write("(" + row + ", " + column + ")");
	}
	
	Console.WriteLine();
}
```

Nested loops are useful when dealing with multidimensional data structures, matrices, tables, or patterns that require layered iteration.

## 🎨 Drawing Patterns

Patterns add a touch of creativity to your code and are often created using nested loops. Patterns are not just visually appealing; they also enhance your problem-solving skills and your understanding of loops, logic, and control flow.

```csharp
int patternSize = 5;

for (int row = 1; row <= patternSize; row++)
{
	for (int column = 1; column <= patternSize; column++)
	{
		Console.Write("* ");
	}
	
	// Move to theh next line after the inner loop completes
	Console.WriteLine();
}
```

## 📜 Guides

Use a for loop when you know the number of iterations in advance.

Use a while loop when the exact number of iterations isn't predetermined, and the loop should continue until a specific condition is met.

Use a do-while loop when you want to guarantee the execution of a block of code at least once, regardless of the initial condition.

The `break` and `continue` keywords are usable only within loops. They are not usable in conditional statements (when not used within a loop).

When used within nested loops, the `break` and `continue` keywords operate in the innermost loop they refer to.