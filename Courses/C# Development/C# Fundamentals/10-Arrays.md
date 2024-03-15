# 🧱 Arrays

## 🗃️ Arrays (Computer Science)

Arrays are containers that allow us to store multiple values called elements under a single name, making it easier to manage and manipulate collections of data.

Arrays are fundamental data structure in C# that allow us to store and manipulate a collection of items of the same data type.

An array is a collection of elements of the same data type stored in contiguous memory locations. It provides a convenient way to work with multiple values of the same type as a single entity.

## 📝 Declaring & Initializing Arrays

In C#, we declare an array by specifying the data type followed by square brackets and the array name.

Arrays in C# are declared using square brackets `[]`, followed by the array name and optionally the array size.

```csharp
// Declaration
int[] numbers;
//      👆 It doesn't contain any elements
```

```csharp
double[] grades;
```

```csharp
char[] symbols;
```

```csharp
string[] words;
```

We can initialize the array, specifying the type and size of the array.

```csharp
int[] numbers = new int[5];
//      👆 Contains placeholders for 5 elements
```

```csharp
double[] grades = new double[3];

char[] symbols = new char[6];

string[] words = new string[4];
```

```csharp
var grades = new double[3];

var symbols = new char[6];

var words = new string[4];
```

```csharp
var numbers = new int[-5];
```

We can initialize an array at the time of declaration, populating it with values, using an array initializer.

```csharp
// Initialize an array of integers
int[] myArray = { 1, 2, 3, 4, 5 };
```

We can also initialize an array explicitly by specifying the size and then assigning values to each element:

```csharp
// Declare an array of integers with size 3
int[] myArray = new int[3];

// Initialize each element
myArray[0] = 10;
myArray[1] = 20;
myArray[2] = 30;
```

## ➡️ Accessing & Modifying Array Elements

Accessing array elements involves specifying the array name followed by square brackets containing the index. Indices in C# are zero-based.

```csharp
int[] numbers = new int[5]; // 👈 Possible indices: [0..4]

// Modifying the first element of the array
//     👇 Index
numbers[0] = 1;

// Accessing the first element of the array
int firstElement = numbers[0];
Console.WriteLine(firstElement); // 👈 Prints "1"
```

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };
int thirdElement = numbers[2];
Console.WriteLine("The third element is: " + thirdElement);
```

```csharp
int[] numbers = new int[3]; // 👈 Possible indexes: [0..2]

numbers[0] = 1;
numbers[1] = 2;
numbers[2] = 3;

Console.WriteLine(numbers[0]); // 👈 Prints "1"
Console.WriteLine(numbers[1]); // 👈 Prints "2"
Console.WriteLine(numbers[2]); // 👈 Prints "3"
```

```csharp
int[] numbers = new int[5]; // 👈 Possible indexes: [0..4]

numbers[0] = 4; // { 4, 0, 0, 0, 0 }
numbers[2] = 3; // { 4, 0, 3, 0, 0 }
numbers[4] = 7; // { 4, 0, 3, 0, 7 }
numbers[3] = 2; // { 4, 0, 3, 2, 7 }
numbers[1] = 6; // { 4, 6, 3, 2, 7 }

numbers[2] = 1; // { 4, 6, 1, 2, 7 }
```

```csharp
int elementsCount = 3;
int[] numbers = new int[elementsCount];
int index = 1;

numbers[index] = 5;
Console.WriteLine(numbers[index]); // 👈 Prints "5"
```

The array needs to be initialized before accessing its elements.

```csharp
int[] numbers;

numbers[0] = 1; // 👈 Causes an error. The array doesn't exist.
```

## 📏 Array Length

In C#, arrays have fixed length. We can retrieve the length of an array using the `Length` property.

The `Length` property is used to get the total number of elements in an array.

```csharp
int[] array = { 1, 2, 3, 4, 5 };

int elementsCount = array.Length;
Console.WriteLine(elementsCount); // 👈 Prints "5"
```

Knowing the array length allows us to:
- Efficiently loop through elements;
- Safely access and manipulate elements without going out of bounds;
- Optimize algorithms by considering the size of the data set.


## 🚧 Array Bounds

Array bounds define the valid range of indices within an array. Attempting to access an index outside the array's range results in an `IndexOutOfRangeException`. An index needs to be in the following interval: \[0..array.Length - 1]. Otherwise, the index is invalid.

```csharp
int[] values = { 1, 2, 3 }; // 👈 Possible indices: [0..2]

int outOfBounds = values[5]; // 👈 Accessing an out-of-bounds index
Console.WriteLine(outOfBounds);
```

## 🖨️ Printing Array Elements

If we try to print the array variable itself we will see a strange output.

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };

Console.WriteLine(numbers);
```

The most common way to print array elements is by iterating through the array using a loop.

```csharp
var elementsCount = 3;
var numbers = new int[elementsCount];

numbers[0] = 1;
numbers[1] = 2;
numbers[2] = 3;

// We could use either elementsCount or numbers.Length
for (int index = 0; index < numbers.Length; index++)
{
	Console.WriteLine(numbers[index]);
}
```

## ✍️ Reading Array Elements

```csharp
var elementsCount = int.Parse(Console.ReadLine());
var numbers = new int[elementsCount];

for (int index = 0; index < numbers.Length; index++)
{
	numbers[index] = int.Parse(Console.ReadLine());
}
```

## ➡️ The "foreach" Keyword

`Pseudocode`

```csharp
foreach (var item in collection)
{
	// Code to execute for each item
}
```

```csharp
var numbers = { 10, 20, 30, 40, 50 };

foreach (var element in numbers)
{
	Console.WriteLine(element);
}
```

```csharp
var fruits = { "Apple", "Banana", "Orange" };

foreach (var fruit in fruits)
{
	Console.WriteLine(fruit);
}
```

The `foreach` keyword can navigate through the characters of a string.

```csharp
var message = "Hello, C#";

foreach (var character in message)
{
	Console.Write(character + " ");
}
```

The `foreach` keyword brings:
- Clarity: Clean and readable code.
- Ease: No need to manage indices manually.
- Compatibility: Works seamlessly with various collections.

While powerful, the `foreach` keyword has limitations, especially when modifying elements during iteration.

## 🔧 The "Array" Class

The `Array` class provides powerful methods for working with arrays efficiently.

The `Array.IndexOf` method returns the index of the first occurrence of a given value in an array, if found; otherwise, the lower bound of the array minus 1.

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };

// Find the index of an element
int index = Array.IndexOf(numbers, 30);

Console.WriteLine(index); // 👈 Prints "2"
```

The `Array.Sort` method sorts the elements in an array.

```csharp
int[] numbers = { 40, 20, 10, 50, 30 };

// Sorting the array
Array.Sort(numbers);

// Displaying the sorted array
foreach (var number in numbers)
{
	Console.WriteLine(number);
}
```

The `Array.Reverse` method reverses the sequence of the elements in an array.

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };

// Reversing the array
Array.Reverse(numbers);

// Displaying the reversed array
foreach (var number in numbers)
{
	Console.WriteLine(number);
}
```

## 📜 Guides

Array indices are zero-based. Always iterate up to `Length - 1` to avoid an `IndexOutOfRangeException`. Always check whether the index value is a valid index in the given context before trying to access the element on the given index.

```csharp
// Good
for (int index = 0; index < myArray.Length; index++)
{
	// Loop Body
}

// Also good
for (int index = 0; index <= myArray.Length - 1; index++)
{
	// Loop Body
}

// Bad (Out of Bounds)
for (int index = 0; index <= myArray.Length; index++)
{
	// Loop Body
}
```

Defensive programming involves anticipating potential issues and implementing measures to guard against them. Handling invalid bounds is a key aspect of defensive programming.

Defensive programming tips:
- Always validate user inputs before using them as indices.
- Use conditional statements to check array bounds before accessing elements.

Use the `Array` class:
- Efficiency: Optimized methods for common array operations.
- Readability.
- Versatility: Applicable to arrays of various data types.