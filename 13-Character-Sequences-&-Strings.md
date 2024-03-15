# 📝 Character Sequences & Strings

## Strings (Computer Science)

**Title: C# Fundamentals: Strings in Computer Science**

---

**Chapter 1: Understanding Strings in Computer Science**

Welcome to the chapter on strings in computer science! In this chapter, we'll delve into the intricacies of strings, a fundamental data type in computer science. We'll explore how strings are represented in memory, the concept of characters, and various aspects of working with strings in C#.

**1.1 Memory Representation of Strings**

In computer memory, strings are typically stored as sequences of characters, where each character is represented by a numeric code called a character encoding. Common character encodings include ASCII, Unicode, and UTF-8. Strings can be stored in contiguous memory locations, allowing for efficient access and manipulation.

**1.2 Characters in Strings**

Characters are the basic building blocks of strings, representing individual symbols such as letters, digits, and punctuation marks. In C#, characters are represented using the char data type, which stores a single 16-bit Unicode character. Unicode allows for the representation of a vast range of characters from various writing systems and languages.

**1.3 String Wrappers**

In C#, strings are represented using the string class, which provides a wide range of methods and properties for working with strings. The string class is part of the System namespace and is immutable, meaning that once a string object is created, its contents cannot be changed. Instead, any operations that modify the string result in the creation of a new string object.

**1.4 Common String Operations**

Strings support various operations, including concatenation, substring extraction, searching, and manipulation. These operations allow you to efficiently work with strings in your C# programs and perform tasks such as data validation, text processing, and formatting.

**1.5 Memory Management for Strings**

In C#, strings are managed by the .NET runtime's garbage collector, which automatically deallocates memory for unused string objects. This ensures efficient memory usage and helps prevent memory leaks by reclaiming memory when strings are no longer needed.

**1.6 Conclusion**

In this chapter, we've explored the fundamentals of strings in computer science, including their memory representation, characters, string wrappers, and common operations. Understanding how strings work at a fundamental level is essential for effective programming in C# and other programming languages. In the following chapters, we'll delve deeper into advanced string manipulation techniques and best practices for working with strings in C#.

---

## String Constructors & Properties

**Title: C# Fundamentals: String Constructors & Properties**

---

**Chapter 1: Introduction to String Constructors**

Welcome to the chapter on string constructors in C#! In this chapter, we'll explore the various constructors available for creating string objects in C#, along with their usage and behavior. We'll discuss the different ways you can initialize strings and provide examples to illustrate each constructor's functionality.

**1.1 Understanding String Constructors**

String constructors in C# allow you to create string objects from various sources, including literal values, character arrays, and other strings. They provide flexibility in how you initialize and manipulate string data in your applications, enabling you to work with strings efficiently and effectively.

**1.2 Common String Constructors**

Some common string constructors in C# include:

- The parameterless constructor, which creates an empty string.
- Constructors that take a character array, allowing you to initialize a string from an array of characters.
- Constructors that take a substring of another string, enabling you to extract portions of a string.
- Constructors that take a string and repeat it a specified number of times, useful for generating repetitive patterns.

Now, let's dive into some examples to see how string constructors work in practice.

---

**Example 1: Creating Strings with Parameterless Constructor**

```csharp
string emptyString = new string();
Console.WriteLine($"Empty string: '{emptyString}'");
```

In this example, we use the parameterless constructor to create an empty string. The resulting string is initialized with no characters, resulting in an empty string.

---

**Example 2: Creating Strings from Character Arrays**

```csharp
char[] charArray = { 'H', 'e', 'l', 'l', 'o' };
string helloString = new string(charArray);
Console.WriteLine($"Hello string: '{helloString}'");
```

In this example, we create a character array representing the word "Hello". We then use the constructor that takes a character array to initialize a string from the array. The resulting string contains the characters from the array.

---

**Example 3: Creating Substrings**

```csharp
string originalString = "Hello, world!";
string substring = new string(originalString.ToCharArray(), 0, 5);
Console.WriteLine($"Substring: '{substring}'");
```

In this example, we create a substring of the original string "Hello, world!" starting from index 0 and taking 5 characters. We use the ToCharArray method to convert the original string to a character array before passing it to the constructor.

---

**Example 4: Repeating Strings**

```csharp
string repeatedString = new string('*', 5);
Console.WriteLine($"Repeated string: '{repeatedString}'");
```

In this example, we use the constructor that takes a character and repeats it a specified number of times to create a string consisting of five asterisks. This is useful for generating repetitive patterns or filling strings with a specific character.

---

In this chapter, we've explored the basics of string constructors in C#, including their usage and examples. Understanding string constructors is essential for working with strings effectively in your C# applications. Stay tuned for more advanced topics on string manipulation and properties in the following chapters!

---

## Character Arithmetics

**Title: C# Fundamentals: Character Arithmetic**

---

**Chapter 1: Introduction to Character Arithmetic**

Welcome to the chapter on character arithmetic in C#! In this chapter, we'll explore the fascinating world of character manipulation and arithmetic operations in C#. We'll delve into the fundamentals of working with characters, including character encoding, ASCII values, and performing arithmetic operations on characters.

**1.1 Understanding Characters in C#**

Characters are fundamental units of text in C#, represented by the char data type. Each character corresponds to a specific Unicode code point, which determines its unique identity and properties. Characters can represent letters, digits, punctuation marks, symbols, and control characters, allowing for the representation of a wide range of textual information.

**1.2 Character Encoding and ASCII Values**

Character encoding is the process of representing characters as binary data for storage or transmission. In C#, characters are encoded using Unicode, a character encoding standard that supports a vast range of characters from different languages and scripts. Each character in Unicode is assigned a unique code point, which is represented as a numerical value.

One of the most widely used character encoding schemes is ASCII (American Standard Code for Information Interchange), which assigns numerical values to characters in the English alphabet, digits, and special symbols. ASCII values range from 0 to 127, with each character mapped to a specific numerical value.

Now, let's explore some examples of character arithmetic in C#.

---

**Example 1: Character Arithmetic with ASCII Values**

```csharp
char ch = 'A';
int asciiValue = (int)ch;
Console.WriteLine($"ASCII value of {ch} is {asciiValue}");

char nextChar = (char)(ch + 1);
Console.WriteLine($"Next character after {ch} is {nextChar}");
```

In this example, we initialize a character variable ch with the value 'A'. We then use type casting to convert the character to its corresponding ASCII value and print it to the console. Next, we perform character arithmetic by adding 1 to the ASCII value of ch to obtain the next character in the ASCII sequence, which is 'B'.

---

**Example 2: Character Manipulation with Arithmetic Operations**

```csharp
char ch = 'a';
int offset = 3;
char shiftedChar = (char)(ch + offset);
Console.WriteLine($"Character {ch} shifted by {offset} positions is {shiftedChar}");
```

In this example, we define a character variable ch with the value 'a' and an integer variable offset with the value 3. We then perform character arithmetic by adding the offset value to the ASCII value of ch to obtain the shifted character. The result is printed to the console, demonstrating how arithmetic operations can be used to manipulate characters in C#.

---

In this chapter, we've explored the basics of character arithmetic in C#, including character encoding, ASCII values, and performing arithmetic operations on characters. We've provided examples to illustrate how characters can be manipulated and transformed using arithmetic operations. Stay tuned for more advanced topics on character manipulation in the following chapters!

---

## The "Char" Class

**Title: C# Fundamentals: The Char Class**

---

**Chapter 1: Introduction to the Char Class**

Welcome to the chapter on the Char class in C#! In this chapter, we'll explore the Char class, which represents a Unicode character in C#. We'll discuss the characteristics of the Char class, its properties and methods, and how it can be used to work with single characters in C# applications.

**1.1 Understanding the Char Class**

The Char class in C# represents a single Unicode character and provides various methods and properties for working with characters. Each instance of the Char class represents a single 16-bit Unicode character, allowing you to perform operations such as comparison, conversion, and manipulation on characters.

**1.2 Characteristics of the Char Class**

The Char class is a value type and is defined in the System namespace. It provides a wide range of methods and properties for working with characters, including methods for converting characters to and from numeric representations, checking character properties such as whitespace and digit status, and performing case conversion operations.

Now, let's dive into some examples to see how the Char class works in practice.

---

**Example 1: Creating and Manipulating Char Instances**

```csharp
char letterA = 'A';
char digitZero = '0';
char newline = '\n';

Console.WriteLine($"Character: {letterA}");
Console.WriteLine($"IsDigit: {Char.IsDigit(letterA)}");
Console.WriteLine($"IsLetter: {Char.IsLetter(letterA)}");
Console.WriteLine($"IsWhiteSpace: {Char.IsWhiteSpace(newline)}");
```

In this example, we create instances of the Char class representing the characters 'A', '0', and '\n' (newline). We then use various methods of the Char class to check the properties of these characters, such as whether they are digits, letters, or whitespace characters.

---

**Example 2: Converting Characters to and from Numeric Representations**

```csharp
char letterB = (char)('A' + 1);
int numericValue = (int)letterB;

Console.WriteLine($"Character: {letterB}");
Console.WriteLine($"Numeric Value: {numericValue}");
```

In this example, we demonstrate how to convert characters to and from their numeric representations using explicit casting. We add 1 to the character 'A' to get the character 'B', and then we convert the character 'B' back to its numeric representation using explicit casting.

---

In this chapter, we've explored the basics of the Char class in C#, including its characteristics and how it can be used to work with single characters. We've also provided examples to illustrate how to create, manipulate, and convert Char instances in C# applications. Stay tuned for more advanced topics on working with characters in the following chapters!

---

## Escape Sequences

Escape sequences provide a way to represent special characters in your code. For example, `'\n'` represents a newline character, and `'\t'` represents a tab.

**Title: C# Fundamentals: Escape Sequences**

---

**Chapter 1: Introduction to Escape Sequences**

Welcome to the chapter on escape sequences in C#! In this chapter, we'll explore the concept of escape sequences, which are special characters used to represent non-printable or special characters within strings. We'll discuss the syntax for escape sequences and demonstrate how they can be used to include special characters in C# strings.

**1.1 Understanding Escape Sequences**

Escape sequences in C# are combinations of the backslash (\) character followed by one or more characters that represent special characters or formatting options within strings. They allow you to include characters that would otherwise be difficult or impossible to represent directly in a string literal, such as newline characters, tabs, or quotation marks.

**1.2 Benefits of Escape Sequences**

Escape sequences offer several benefits in C# programming. Firstly, they provide a convenient way to include special characters in strings without the need for complex string manipulation or concatenation. This makes code more readable and maintainable, as the intent of the string is clear at a glance.

Secondly, escape sequences allow you to represent characters that may not be directly typable on the keyboard, such as newline characters or tabs. This makes it easier to create formatted text or output that adheres to specific formatting conventions or requirements.

Now, let's dive into some examples to see how escape sequences work in practice.

---

**Example 1: Including Newline Characters**

```csharp
string multilineString = "This is line 1.\nThis is line 2.";
Console.WriteLine(multilineString);
```

In this example, we use the escape sequence \n to include a newline character in the string. When the string is printed to the console, the newline character causes the text to be split into two lines, resulting in formatted output with each line of text on a separate line.

---

**Example 2: Including Tabs**

```csharp
string tabbedString = "Name\tAge\tCity";
Console.WriteLine(tabbedString);
```

In this example, we use the escape sequence \t to include a tab character in the string. When the string is printed to the console, the tab character causes the text to be aligned in columns, resulting in formatted output with each field separated by a tab.

---

In this chapter, we've explored the basics of escape sequences in C#, including their syntax and benefits. We've also provided examples to illustrate how escape sequences can be used to include special characters in strings. Stay tuned for more advanced topics on escape sequences in the following chapters!

---

## String Comparison

**Title: C# Fundamentals: String Comparison**

---

**Chapter 1: Introduction to String Comparison**

Welcome to the chapter on string comparison in C#! In this chapter, we'll explore the various methods and techniques available for comparing strings in C#. We'll discuss different comparison options, such as ordinal comparison, culture-sensitive comparison, and case-insensitive comparison, and provide examples to demonstrate how to use them effectively.

**1.1 Understanding String Comparison**

String comparison is the process of determining whether two strings are equal or determining the relative order of two strings based on their character sequences. In C#, strings can be compared using different comparison methods, each with its own rules and considerations. Understanding these methods is essential for writing robust and reliable code that handles string comparison scenarios correctly.

**1.2 Common String Comparison Methods**

In C#, there are several methods available for comparing strings, each serving different purposes:

- **Ordinal Comparison**: Compares strings based on their Unicode values without considering culture or case differences.
- **Culture-Sensitive Comparison**: Compares strings based on linguistic rules specific to a culture or locale.
- **Case-Insensitive Comparison**: Compares strings while ignoring differences in character casing.

Now, let's dive into some examples to see how these string comparison methods work in practice.

---

**Example 1: Ordinal Comparison**

```csharp
string str1 = "apple";
string str2 = "Apple";

int result = string.Compare(str1, str2, StringComparison.Ordinal);

if (result == 0)
{
    Console.WriteLine("Strings are equal.");
}
else
{
    Console.WriteLine("Strings are not equal.");
}
```

In this example, we use the `string.Compare()` method with `StringComparison.Ordinal` to perform an ordinal comparison between two strings (`str1` and `str2`). Since ordinal comparison considers the Unicode values of characters without regard to culture or case, the result will be "Strings are not equal."

---

**Example 2: Culture-Sensitive Comparison**

```csharp
string str1 = "resume";
string str2 = "résumé";

int result = string.Compare(str1, str2, StringComparison.CurrentCulture);

if (result == 0)
{
    Console.WriteLine("Strings are equal.");
}
else
{
    Console.WriteLine("Strings are not equal.");
}
```

In this example, we use the `string.Compare()` method with `StringComparison.CurrentCulture` to perform a culture-sensitive comparison between two strings (`str1` and `str2`). Since the strings have different linguistic representations due to the accent mark in "résumé," the result will be "Strings are not equal."

---

**Example 3: Case-Insensitive Comparison**

```csharp
string str1 = "apple";
string str2 = "APPLE";

int result = string.Compare(str1, str2, StringComparison.OrdinalIgnoreCase);

if (result == 0)
{
    Console.WriteLine("Strings are equal.");
}
else
{
    Console.WriteLine("Strings are not equal.");
}
```

In this example, we use the `string.Compare()` method with `StringComparison.OrdinalIgnoreCase` to perform a case-insensitive comparison between two strings (`str1` and `str2`). Since case is ignored during comparison, the result will be "Strings are equal."

---

In this chapter, we've explored the basics of string comparison in C#, including different comparison methods and their usage. We've also provided examples to illustrate how to perform ordinal, culture-sensitive, and case-insensitive comparisons effectively. Understanding these string comparison techniques will enable you to write code that handles string comparison scenarios correctly in your C# applications.

---

## String Immutability

**Title: C# Fundamentals: String Immutability**

---

**Chapter 1: Understanding String Immutability**

Welcome to the chapter on string immutability in C#! In this chapter, we'll explore the concept of string immutability and its implications in C# programming. We'll discuss what string immutability means, why strings are immutable in C#, and how immutability affects string manipulation and memory management.

**1.1 What is String Immutability?**

In C#, a string is immutable, which means that once it is created, its value cannot be changed. Any operation that appears to modify a string actually creates a new string object with the modified value, leaving the original string unchanged. This behavior is in contrast to mutable types, such as arrays or lists, where elements can be modified in place.

**1.2 Implications of String Immutability**

String immutability has several implications for C# developers. Firstly, it ensures thread safety, as multiple threads can safely read the same string object without the risk of data corruption or inconsistency due to concurrent modifications.

Secondly, string immutability simplifies memory management, as it reduces the need for defensive copying and synchronization when working with strings in multithreaded scenarios. Since strings are immutable, they can be safely shared among multiple threads without the risk of unintended modifications.

Now, let's explore some examples to understand how string immutability works in practice.

---

**Example 1: Modifying Strings**

```csharp
string original = "Hello";
string modified = original + ", World!";

Console.WriteLine("Original string: " + original); // Output: Original string: Hello
Console.WriteLine("Modified string: " + modified); // Output: Modified string: Hello, World!
```

In this example, we concatenate the original string "Hello" with ", World!" to create a modified string. However, the original string remains unchanged, and a new string object is created to hold the modified value. This demonstrates how string immutability ensures that the original string is not modified.

---

**Example 2: Passing Strings to Methods**

```csharp
void ModifyString(string str)
{
    str += " (modified)";
}

string original = "Hello";
ModifyString(original);

Console.WriteLine("Original string: " + original); // Output: Original string: Hello
```

In this example, we pass a string to a method that attempts to modify it by appending "(modified)" to the end. However, since strings are immutable, the original string remains unchanged, and the modification is only applied to a local copy of the string within the method scope. This highlights how string immutability affects method parameters and ensures that string values are not inadvertently modified.

---

In this chapter, we've explored the concept of string immutability in C#, including its definition and implications for C# programming. We've also provided examples to illustrate how string immutability works in practice and how it affects string manipulation and memory management. Stay tuned for more insights on string immutability and its practical implications in the following chapters!

---