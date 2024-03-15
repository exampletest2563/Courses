# 🔀 Control Flow - Conditional Statements

## 💡 Conditional Statements

In any programming language, the code needs to make decisions and carry out actions depending on different inputs. Conditional statements allow our code to make decisions based on specific conditions. Think of them as the gatekeepers or the guards of our code.

`Pseudocode`

```csharp
if (condition)
{
	// Code to be executed if condition is true
}
else
{
	// Code to be executed if condition is false
}
```

In this example the word `condition` could be replaced with one of the following:
- a literal of type `bool`;
- a variable of type `bool`;
- any expression that could be evaluated to a value of type `bool`.

## IF Statement

The IF statement consists of the keyword `if`, a condition enclosed in parentheses, and a block of code to execute if the condition is true.

```csharp
var studentScore = int.Parse(Console.ReadLine());

if (studentScore >= 50)
{
	Console.WriteLine("Pass!"); 
}
```

```csharp
var userAge = int.Parse(Console.ReadLine());

if (userAge >= 18)
{
	Console.WriteLine("You're eligible for access!");
}
```

Formatting doesn't matter.

```csharp
var userAge = int.Parse(Console.ReadLine());

if (userAge >= 18) Console.WriteLine("You're eligible for access!");
```

We can omit the curly brackets.

```csharp
var userAge = int.Parse(Console.ReadLine());

if (userAge >= 18)
	Console.WriteLine("You're eligible for access!");
```

The IF statement executes the first statement written after the condition. The curly brackets are used to wrap statements and execute them at once.

```csharp
var userAge = int.Parse(Console.ReadLine()); // Example: "12"

if (userAge >= 18)
	Console.WriteLine("You're eligible for access!");
	Console.WriteLine("You are older than 18 years old.");
```

## IF-ELSE Statement

IF-ELSE statements enable our programs to take one path if a condition is true and another if it's false. They feature the familiar `if` keyword, a condition in parentheses, a block of code for the true scenario, followed by the `else` keyword and another block of code for the false scenario.

```csharp
var studentScore = int.Parse(Console.ReadLine());

if (studentScore >= 50)
{
	Console.WriteLine("Pass!"); 
}
else
{
	Console.WriteLine("Fail!");
}
```

```csharp
var studentScore = int.Parse(Console.ReadLine());
var output = "";

if (studentScore >= 50)
{
	output = "Pass!";
}
else
{
	output = "Fail!";
}

Console.WriteLine(output);
```

## 🧭 Variables Scope & Visibility

Scope defines the region of your code where a variable is accessible.

Local variables live within a specific block of code - the innermost block of code they have been declared in. If we declare a variable inside an `if` statement, it's local to that block.

```csharp
var outerScopeVariable = 20;

if (condition)
{
	// Block-scoped / Local variable
    var innerScopeVariable = 10;
    
    // innerScopeVariable is accessible here
    Console.WriteLine(innerScopeVariable);
    
    // outerScopeVariable is accessible here
    Console.WriteLine(outerScopeVariable);
}

// innerScopeVariable is not accessible here

// outerScopeVariable is accessible here
Console.WriteLine(outerScopeVariable);
```

## Multiple Conditions

```csharp
var studentScore = int.Parse(Console.ReadLine());
var output = "";

if (studentScore >= 90)
{
	output = "Excellent!";
}
else if (studentScore >= 50)
{
	output = "Pass!";
}
else
{
	output = "Fail!";
}

Console.WriteLine(output);
```

## Nested Conditional Statements

We can nest IF statements within each other to create more complex conditions and handle various scenarios.

```csharp
var studentScore = int.Parse(Console.ReadLine());
var output = string.Empty;

if (studentScore >= 0 && studentScore <= 100)
{
	if (studentScore >= 90)
	{
		output = "Excellent!";
	}
	else if (studentScore >= 50)
	{
		output = "Pass!";
	}
	else
	{
		output = "Fail!";
	}
}
else
{
	output = "Invalid Score!";
}

Console.WriteLine(output);
```

```csharp
var studentScore = int.Parse(Console.ReadLine());
var output = "";

if (studentScore < 0 || studentScore > 100)
{
	output = "Invalid Score!";
}
else
{
	if (studentScore >= 90)
	{
		output = "Excellent!";
	}
	else if (studentScore >= 50)
	{
		output = "Pass!";
	}
	else
	{
		output = "Fail!";
	}
}

Console.WriteLine(output);
```

```csharp
var userAge = 22;
var hasAccount = false;

if (userAge >= 18)
{
	if (hasAccount)
	{
		Console.WriteLine("Welcome!");
	}
	else
	{
		Console.WriteLine("You need to create an account.");
	}
}
else
{
	Console.WriteLine("Access restricted to users 18 and older.");
}
```

## 🛠️ Building Complex Boolean Expressions

We can use logical operators to create complex boolean conditions.

```csharp
var isPremiumMember = true;
var isVipMember = false;

if (isPremiumMember || isVipMember)
{
	Console.WriteLine("You have special privileges!");
}
```

```csharp
bool orderContainsMerchandiseProduct = true;
bool isActivePromotion = true;
bool hasOrderDiscount = orderContainsMerchandiseProduct && isActivePromotion;
Console.WriteLine(hasOrderDiscount);
```

```csharp
var age = 25;
var isAccountActive = true;
var hasMembership = true;

if (age >= 18 && isAccountActive && hasMembership)
{
    Console.WriteLine("Welcome! You have access.");
}
```

Parentheses `()` are essential for clarifying the order of evaluation.

```csharp
var isWeekend = true;
var isHoliday = false;
var temperatureCelsius = 32;

var goOutside = (isWeekend || isHoliday) && (temperatureCelsius > 25);
Console.WriteLine(goOutside); // 👈 Prints "True"
```

Storing the result of the evaluation in an variable may add to the code readability.

```csharp
var age = int.Parse(Console.ReadLine());
var isValid = age >= 1 && age <= 100;

if (!isValid)
{
	Console.WriteLine("Invalid age!");
}
```

```csharp
var age = 22;
var isMember = true;

if ((age >= 18 && age <= 30) || isMember)
{
	Console.WriteLine("You qualify for a discount!");
}
```

```csharp
var isPremiumMember = true;
var isVipMember = false;
var age = int.Parse(Console.ReadLine());
var isAccountBlocked = false;

if ((isPremiumMember || isVIPMember) && age >= 25 && age <= 40 && !isAccountBlocked)
{
	Console.WriteLine("Welcome! You meet the criteria.");
}
```

C# supports short-circuiting, where the second operand is only evaluated if necessary. This can improve performance and prevent unnecessary computations.

The following example will not call the functionality `CheckResourceAvailability()` if the variable `isAvailable` is evaluated to false.

```csharp
if (isAvailable && CheckResourceAvailability())
{
	// Code
}
```

## 🔍 Switch Statement

Sometimes, our code needs to make decisions based on the value of a variable.

`Pseudocode`

```csharp
if (variable == value1)
{
	Console.WriteLine("Case 1");
}
else if (variable == value2)
{
	Console.WriteLine("Case 2");
}
...
else if (variable == valueN)
{
	Console.WriteLine("Case N");
}
else
{
	Console.WriteLine("Default Case");
}
```

The `switch` statement evaluates a variable against multiple possible values and executes the block of code associated with the first matching case.

`Pseudocode`

```csharp
switch (expression)
{
	case value1:
		Console.WriteLine("Case 1");
		break;
	case value2:
		Console.WriteLine("Case 2");
		break;
	...
	case N:
		Console.WriteLine("Case N");
		break;
	default:
		Console.WriteLine("Default Case");
		break;
}
```

```csharp
var dayOfWeek = int.Parse(Console.ReadLine());

switch (dayOfWeek)
{
	case 1:
		Console.WriteLine("Monday");
		break;
	case 2:
		Console.WriteLine("Tuesday");
		break;
	case 3:
		Console.WriteLine("Wednesday");
		break;
	case 4:
		Console.WriteLine("Thursday");
		break;
	case 5:
		Console.WriteLine("Friday");
		break;
	case 6:
		Console.WriteLine("Saturday");
		break;
	case 7:
		Console.WriteLine("Sunday");
		break;
	default:
		Console.WriteLine("Invalid day!");
		break;
}
```

Unlike some other languages, C# switch statements don't automatically fall through to subsequent cases. Each case must end with a `break` or other exit statement.

We can group multiple cases to execute the same block of code.

```csharp
var dayOfWeek = int.Parse(Console.ReadLine());

switch (dayOfWeek)
{
	case 1:
	case 2:
	case 3:
	case 4:
	case 5:
		Console.WriteLine("It's a weekday.");
		break;
	case 6:
	case 7:
		Console.WriteLine("It's the weekend!");
		break;
	default:
		Console.WriteLine("Invalid day!");
		break;
}
```

```csharp
var dayOfWeek = int.Parse(Console.ReadLine());

if (dayOfWeek == 1 || dayOfWeek == 2 || dayOfWeek == 3 || dayOfWeek == 4 || dayOfWeek == 5)
{
	Console.WriteLine("It's a weekday.");
}
else if (dayOfWeek == 6 || dayOfWeek == 7)
{
	Console.WriteLine("It's the weekend!");
}
else
{
	Console.WriteLine("Invalid day!");
}
```

Starting from C# 8.0, we can use switch expressions, a more expressive form of the switch statement.

```csharp
var dayOfWeek = int.Parse(Console.ReadLine());

var dayType = dayOfWeek switch
{
	>= 1 and <= 5 => "Weekday",
	>= 6 and <= 7 => "Weekend",
	_ => "Invalid day!
};

Console.WriteLine(dayType);
```

Switch statements enhance code readability, especially when dealing with multiple possible values. They make our code more structured and easier to maintain.

## 🌟 Conditional Operator

The conditional operator, often called the ternary operator, provides a way to make decisions within a single line of code.

`Pseudocode`

```csharp
var result = (condition) ? trueExpression : falseExpression;
```

```csharp
var isDaytime = true;
var output = isDaytime ? "Day" : "Night";

Console.WriteLine(output); // Prints "Day"
```

```csharp
var isDaytime = true;
var output = "";

if (isDayTime)
{
	output = "Day";
}
else
{
	output = "Night";
}

Console.WriteLine(output); // 👈 Prints "Day"
```

```csharp
var itemPrice = 50;
var isMember = true;

var totalPrice = isMember ? itemPrice * 0.8 : itemPrice;
Console.WriteLine(totalPrice); // 👈 Prints "40"
```

```csharp
var number = int.Parse(Console.ReadLine());
Console.WriteLine("The number is " + (number % 2 == 0 ? "even" : "odd") + ".");
```

We can nest conditional operators for more complex scenarios, but be cautious not to sacrifice readability.

```csharp
var temperature = int.Parse(Console.ReadLine()); // 👈 Example: "23"

var weatherType = (temperature > 25) ? "Hot" : (temperature < 10) ? "Cold" : "Moderate";

Console.WriteLine(weatherType); // 👈 Prints "Moderate"
```

In case expressions are too long, we can format the line differently.

```csharp
var result = expression
	? veryLongTrueExpression
	: veryLongFalseExpression;

Console.WriteLine(result);
```

## 📜 Guides

Always use curly brackets `{}` when declaring a body of a structure or a statement. Always leave an empty line after the closing bracket.

Aim to minimize the scope of your variables. Declare variables in the block of code they are used. The later you declare the variable the better.

Avoid complex nesting and complex conditions.

Use brackets to override the precedence of an operator where needed. Using brackets enhance code readability.

Use the conditional operator when making simple decisions with clear true/false outcomes. This could make your code more compact and readable. For more complex scenarios, consider using other decision-making constructs like if-else statements or switch. In such cases, traditional control flow structures might be more readable.