# Generics

## Generics

**Title: C# Fundamentals: Generics - Understanding and Benefits**

---

**Chapter 1: Introduction to C# Generics**

Welcome to the world of C# generics! In this chapter, we'll explore the fundamentals of generics in C# programming. Generics are a powerful feature that allows you to write flexible and reusable code by parameterizing types. Let's dive in and understand what generics are and why they're essential in C# development.

**1.1 Understanding Generics**

Generics in C# provide a way to create classes, methods, and data structures that can work with any data type. Instead of specifying concrete types when defining a class or method, you can use type parameters, which are placeholders for specific types. This enables you to write code that is more flexible and adaptable to various data types.

**1.2 Benefits of Generics**

Generics offer several benefits that make them indispensable in C# programming. Firstly, generics promote code reusability by allowing you to write generic algorithms and data structures that can be used with different types. This reduces code duplication and improves maintainability.

Secondly, generics enhance type safety by providing compile-time type checking. With generics, you can catch type-related errors at compile time rather than runtime, resulting in more robust and reliable code.

Lastly, generics improve performance by eliminating the need for boxing and unboxing operations when working with value types. This leads to better performance and memory usage, especially in scenarios involving large datasets or performance-critical applications.

In this chapter, we've introduced the concept of generics in C# and discussed some of the key benefits they offer. As we delve deeper into the topic in the following chapters, you'll learn how to leverage generics to write more flexible, efficient, and maintainable code in your C# applications.

---

In the subsequent chapters, we'll explore the practical aspects of using generics in C#, including creating generic classes and methods, applying constraints, working with generic collections, and understanding covariance and contravariance. By the end of this book, you'll have a comprehensive understanding of generics in C# and how to harness their power to write high-quality, reusable code.

Stay tuned for more insights and hands-on examples as we unravel the world of C# generics together!

---

## Generic Classes

**Title: C# Fundamentals: Generic Classes**

---

**Chapter 1: Introduction to Generic Classes**

Welcome to the chapter on generic classes in C#! In this chapter, we'll dive into the world of generic classes, a powerful feature of C# that allows you to create classes that can work with any data type. We'll explore the syntax for defining generic classes and demonstrate how they enable code reusability and flexibility.

**1.1 Understanding Generic Classes**

Generic classes in C# are classes that can be parameterized with one or more type parameters. These type parameters serve as placeholders for specific types that will be provided when an instance of the class is created. This allows you to write classes that can work with different data types without having to define separate implementations for each type.

**1.2 Benefits of Generic Classes**

Generic classes offer several benefits that make them invaluable in C# programming. Firstly, they promote code reusability by allowing you to write classes that can be used with any data type. This reduces code duplication and improves maintainability.

Secondly, generic classes enhance type safety by providing compile-time type checking. Any type-related errors are caught at compile time, reducing the likelihood of runtime errors and improving the overall robustness of the code.

Lastly, generic classes improve performance by eliminating the need for boxing and unboxing operations when working with value types. This leads to better performance and memory usage, especially in scenarios involving large datasets or performance-critical applications.

Now, let's dive into some examples to see how generic classes work in practice.

---

**Example 1: Generic Stack Class**

```csharp
public class Stack<T>
{
    private T[] items;
    private int top;

    public Stack(int capacity)
    {
        items = new T[capacity];
        top = -1;
    }

    public void Push(T item)
    {
        if (top == items.Length - 1)
        {
            throw new StackOverflowException("Stack is full.");
        }
        items[++top] = item;
    }

    public T Pop()
    {
        if (top == -1)
        {
            throw new InvalidOperationException("Stack is empty.");
        }
        return items[top--];
    }

    public int Count => top + 1;
}
```

In this example, we define a generic Stack class that can work with any data type. The class uses a type parameter T to represent the type of items stored in the stack. We provide implementations for Push and Pop methods, which work with items of type T.

---

**Example 2: Using the Generic Stack Class**

```csharp
Stack<int> intStack = new Stack<int>(5);
intStack.Push(10);
intStack.Push(20);
intStack.Push(30);

Console.WriteLine("Popped item: " + intStack.Pop()); // Output: Popped item: 30

Stack<string> stringStack = new Stack<string>(3);
stringStack.Push("Hello");
stringStack.Push("World");

Console.WriteLine("Popped item: " + stringStack.Pop()); // Output: Popped item: World
```

In this example, we create instances of the generic Stack class for storing integers and strings. We push items onto the stacks and then pop items from them, demonstrating how the generic Stack class works with different data types.

---

In this chapter, we've explored the basics of generic classes in C#, including their syntax and benefits. We've also provided examples to illustrate how generic classes can be used to create flexible and reusable code. Stay tuned for more in-depth exploration of generic classes in the following chapters!

---

## Constraints

**Title: C# Fundamentals: Generic Constraints**

---

**Chapter 1: Introduction to Generic Constraints**

Welcome to the chapter on generic constraints in C#! In this chapter, we'll explore the concept of generic constraints and how they allow you to impose restrictions on the types that can be used with generic type parameters. We'll discuss the syntax for defining generic constraints and demonstrate how they enable more precise control over generic types.

**1.1 Understanding Generic Constraints**

Generic constraints in C# allow you to specify requirements that type parameters must meet when used with generic classes or methods. These constraints can include specifying that a type parameter must be a class, a struct, have a default constructor, or implement a particular interface. By applying constraints, you can ensure that generic code behaves as expected and provide compile-time type checking for generic types.

**1.2 Benefits of Generic Constraints**

Generic constraints offer several benefits that make them essential in C# programming. Firstly, they improve code safety by enforcing type constraints at compile time. This reduces the likelihood of runtime errors caused by using incompatible types with generic code.

Secondly, generic constraints enable more precise control over generic types, allowing you to define specific behaviors or capabilities required by type parameters. This makes your code more expressive and self-documenting, as the constraints provide clear expectations for how generic types should be used.

Now, let's dive into some examples to see how generic constraints work in practice.

---

**Example 1: Generic Stack Class with Constraint**

```csharp
public class Stack<T> where T : struct
{
    private T[] items;
    private int top;

    public Stack(int capacity)
    {
        items = new T[capacity];
        top = -1;
    }

    public void Push(T item)
    {
        if (top == items.Length - 1)
        {
            throw new StackOverflowException("Stack is full.");
        }
        items[++top] = item;
    }

    public T Pop()
    {
        if (top == -1)
        {
            throw new InvalidOperationException("Stack is empty.");
        }
        return items[top--];
    }

    public int Count => top + 1;
}
```

In this example, we define a generic Stack class with a constraint that restricts the type parameter T to be a value type (struct). This ensures that only value types can be used with the Stack class, providing compile-time type safety.

---

**Example 2: Using the Generic Stack Class with Constraint**

```csharp
Stack<int> intStack = new Stack<int>(5);
intStack.Push(10);
intStack.Push(20);
intStack.Push(30);

Console.WriteLine("Popped item: " + intStack.Pop()); // Output: Popped item: 30

Stack<string> stringStack = new Stack<string>(3); // Error: string is not a value type
```

In this example, we create an instance of the generic Stack class with a value type (int) as the type parameter. We push items onto the stack and then pop an item from it, demonstrating how the generic Stack class with a constraint works.

---

In this chapter, we've explored the basics of generic constraints in C#, including their syntax and benefits. We've also provided examples to illustrate how generic constraints can be used to impose restrictions on generic types and ensure type safety. Stay tuned for more advanced topics on generic constraints in the following chapters!

---

## Generic Collections

**Title: C# Fundamentals: Generic Collections**

---

**Chapter 1: Introduction to Generic Collections**

Welcome to the chapter on generic collections in C#! In this chapter, we'll explore the power of generic collections, which provide flexible and type-safe ways to store and manipulate data in C# applications. We'll discuss the benefits of using generic collections and introduce some of the commonly used generic collection types available in the .NET framework.

**1.1 Understanding Generic Collections**

Generic collections in C# are data structures that can store elements of any data type while providing type safety and compile-time checking. Unlike non-generic collections, which store elements as objects and require explicit casting, generic collections allow you to work with elements of specific types without sacrificing type safety.

**1.2 Benefits of Generic Collections**

Generic collections offer several advantages over non-generic collections. Firstly, they provide type safety by allowing you to specify the type of elements stored in the collection. This eliminates the need for explicit casting and reduces the risk of runtime errors caused by type mismatches.

Secondly, generic collections offer better performance and memory efficiency compared to non-generic collections. Since elements are stored as their actual types rather than as objects, there is no overhead associated with boxing and unboxing operations.

Now, let's dive into some examples to see how generic collections work in practice.

---

**Example 1: Using List<T> Generic Collection**

```csharp
List<int> numbers = new List<int>();
numbers.Add(10);
numbers.Add(20);
numbers.Add(30);

foreach (int number in numbers)
{
    Console.WriteLine(number);
}
```

In this example, we create a List<T> collection of integers and add some elements to it. We then iterate over the collection using a foreach loop and print each element to the console. The List<T> collection dynamically resizes to accommodate the added elements, providing a flexible and convenient way to store and manipulate data.

---

**Example 2: Using Dictionary<TKey, TValue> Generic Collection**

```csharp
Dictionary<string, int> ages = new Dictionary<string, int>();
ages.Add("Alice", 30);
ages.Add("Bob", 25);
ages.Add("Charlie", 35);

foreach (var kvp in ages)
{
    Console.WriteLine($"{kvp.Key}: {kvp.Value}");
}
```

In this example, we create a Dictionary<TKey, TValue> collection to store key-value pairs of strings and integers representing the ages of individuals. We add some key-value pairs to the dictionary and then iterate over it using a foreach loop, printing each key-value pair to the console. The Dictionary<TKey, TValue> collection provides fast lookup and retrieval of values based on keys, making it ideal for scenarios requiring key-based data access.

---

In this chapter, we've explored the basics of generic collections in C#, including their benefits and some commonly used collection types. We've also provided examples to illustrate how generic collections can be used to store and manipulate data in C# applications. Stay tuned for more advanced topics on generic collections in the following chapters!

---

## Covariance & Contravariance


**Title: C# Fundamentals: Generic Covariance & Contravariance**

---

**Chapter 1: Introduction to Covariance and Contravariance**

Welcome to the chapter on covariance and contravariance in C#! In this chapter, we'll explore two powerful concepts that allow you to work with generic types in more flexible and expressive ways. We'll discuss the concepts of covariance and contravariance and how they enable you to assign more specific or more general types to generic type parameters.

**1.1 Understanding Covariance and Contravariance**

Covariance and contravariance are terms used to describe the relationships between types when considering inheritance and generic type parameters. Covariance allows you to assign a more derived (specific) type to a less derived (more general) type, while contravariance allows you to do the opposite.

**1.2 Benefits of Covariance and Contravariance**

Covariance and contravariance provide several benefits in C# programming. Firstly, they allow for more flexible and intuitive use of generic types, enabling you to write code that is more generic and reusable. Secondly, they improve code readability and maintainability by allowing you to express relationships between types more accurately and concisely.

Now, let's dive into some examples to see how covariance and contravariance work in practice.

---

**Example 1: Covariance with Interfaces**

```csharp
interface IAnimal
{
    string Name { get; }
}

class Dog : IAnimal
{
    public string Name { get; }

    public Dog(string name)
    {
        Name = name;
    }
}

class Cat : IAnimal
{
    public string Name { get; }

    public Cat(string name)
    {
        Name = name;
    }
}

List<Dog> dogs = new List<Dog>
{
    new Dog("Buddy"),
    new Dog("Max")
};

IEnumerable<IAnimal> animals = dogs;
foreach (var animal in animals)
{
    Console.WriteLine(animal.Name);
}
```

In this example, we define an interface IAnimal and two classes, Dog and Cat, that implement the interface. We then create a List<Dog> containing instances of Dog objects. Using covariance, we assign the List<Dog> to an IEnumerable<IAnimal>, allowing us to iterate over the list and treat each Dog object as an IAnimal. This demonstrates how covariance allows us to assign a more specific type (List<Dog>) to a more general type (IEnumerable<IAnimal>).

---

**Example 2: Contravariance with Delegates**

```csharp
delegate void AnimalHandler(IAnimal animal);

void HandleAnimal(IAnimal animal)
{
    Console.WriteLine($"Handling {animal.Name}");
}

void FeedAnimal(IAnimal animal)
{
    Console.WriteLine($"Feeding {animal.Name}");
}

Action<Dog> dogAction = HandleAnimal;
Action<Cat> catAction = HandleAnimal;

dogAction(new Dog("Buddy"));
catAction(new Cat("Whiskers"));
```

In this example, we define a delegate AnimalHandler that represents methods accepting an IAnimal parameter. We then define two methods, HandleAnimal and FeedAnimal, that accept an IAnimal parameter. Using contravariance, we assign the HandleAnimal method to Action<Dog> and Action<Cat>, allowing us to pass Dog and Cat objects to the delegate even though they are more specific types than IAnimal. This demonstrates how contravariance allows us to assign a more general type (Action<IAnimal>) to a more specific type (Action<Dog> and Action<Cat>).

---

In this chapter, we've explored the concepts of covariance and contravariance in C#, including their benefits and some examples of how they can be used. Understanding covariance and contravariance is essential for writing flexible and reusable code with generic types in C#. Stay tuned for more advanced topics on covariance and contravariance in the following chapters!

---