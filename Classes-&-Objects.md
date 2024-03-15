# 🍏 Classes & Objects

## Defining Classes

C# allows us to create our own custom data types through classes and structures.

`Rectangle.cs`

```csharp
public class Rectangle
{
	public int Width { get; set; }

	public int Height { get; set; }
}
```

`Startup.cs`

```csharp
var rectangle = new Rectangle();

rectangle.Width = 3;
rectangle.Height = 4;

var area = rectangle.Width * rectangle.Height;
Console.WriteLine(area);
```

## Methods

`Rectangle.cs`

```csharp
public class Rectangle
{
	public int Width { get; set; }

	public int Height { get; set; }

	public int GetArea()
	{
		return Width * Height;
	}

	public int GetPerimeter()
	{
		return 2 * (Width + Height);
	}
}
```

`Startup.cs`

```csharp
var rectangle = new Rectangle();

rectangle.Width = 3;
rectangle.Height = 4;

var area = rectangle.GetArea();
Console.WriteLine(area);

var perimeter = rectangle.GetPerimeter();
Console.WriteLine(perimeter);
```

## Class Instances

## Fields & Properties

## The "this" Keyword

`Rectangle.cs`

```csharp
public class Rectangle
{
	public int Width { get; set; }

	public int Height { get; set; }

	public int GetArea()
	{
		return this.Width * this.Height;
	}

	public int GetPerimeter()
	{
		return 2 * (this.Width + this.Height);
	}
}
```

## Constructors

`Rectangle.cs`

```csharp
public class Rectangle
{
	public int Width { get; set; }

	public int Height { get; set; }

	public Rectangle(int width, int height)
	{
		this.Width = width;
		this.Height = height;
	}

	public int GetArea()
	{
		return this.Width * this.Height;
	}

	public int GetPerimeter()
	{
		return 2 * (this.Width + this.Height);
	}
}
```

`Startup.cs`

```csharp
var rectangle = new Rectangle(3, 4);

var area = rectangle.GetArea();
Console.WriteLine(area);

var perimeter = rectangle.GetPerimeter();
Console.WriteLine(perimeter);
```

## Object Initializer

## Guides

### Chapter: Classes & Objects in C#

#### 1. Introduction to Classes and Objects
   - 1.1 Understanding Object-Oriented Programming (OOP) Concepts
   - 1.2 Overview of Classes and Objects in C#
   - 1.3 Importance of Classes and Objects in Software Development

**Title: C# Fundamentals: Introduction to Classes and Objects**

---

**Chapter 1: Understanding Classes and Objects**

Welcome to the world of object-oriented programming with C#! In this chapter, we'll introduce you to the fundamental concepts of classes and objects, which form the backbone of modern software development. You'll learn what classes and objects are, how they relate to each other, and how to create and use them effectively in your C# programs.

**1.1 What are Classes and Objects?**

In C#, a class is a blueprint or template for creating objects. It defines the structure and behavior of objects of a certain type. An object, on the other hand, is an instance of a class, representing a specific entity or concept in your program. Objects encapsulate data (attributes) and behavior (methods), providing a way to model real-world entities in code.

**1.2 Syntax of Class Declaration**

In C#, you declare a class using the `class` keyword followed by the class name and a pair of curly braces. Inside the braces, you define the members of the class, such as fields, properties, methods, and constructors.

```csharp
public class Person
{
    // Fields
    public string Name;
    public int Age;

    // Constructor
    public Person(string name, int age)
    {
        Name = name;
        Age = age;
    }

    // Method
    public void DisplayInfo()
    {
        Console.WriteLine($"Name: {Name}, Age: {Age}");
    }
}
```

In this example, we define a `Person` class with fields for `Name` and `Age`, a constructor to initialize these fields, and a method `DisplayInfo` to print the person's information.

**1.3 Creating and Using Objects**

Once a class is defined, you can create objects (instances) of that class using the `new` keyword followed by the class name and optional constructor arguments. You can then access the members of the object using the dot (`.`) operator.

```csharp
class Program
{
    static void Main(string[] args)
    {
        // Creating objects
        Person person1 = new Person("Alice", 30);
        Person person2 = new Person("Bob", 25);

        // Using objects
        person1.DisplayInfo();
        person2.DisplayInfo();
    }
}
```

In this example, we create two `Person` objects (`person1` and `person2`) and call the `DisplayInfo` method on each object to print their information.

---

In this chapter, we've introduced you to the basics of classes and objects in C#. You've learned how to define classes, create objects from those classes, and access their members. Stay tuned for more advanced topics on classes and objects in the following chapters!

---

#### 2. Defining Classes
   - 2.1 Syntax of Class Declaration in C#
   - 2.2 Creating Fields and Properties in Classes
   - 2.3 Implementing Constructors for Initialization
   - 2.4 Adding Methods to Perform Actions
   - 2.5 Understanding Access Modifiers for Class Members

**Title: C# Fundamentals: Defining Classes**

---

**Chapter 1: Introduction to Defining Classes**

Welcome to the chapter on defining classes in C#! In this chapter, we'll explore the fundamentals of defining classes, which are essential building blocks in object-oriented programming. We'll discuss how classes encapsulate data and behavior, allowing you to model real-world entities in your C# applications.

**1.1 Understanding Object-Oriented Programming (OOP) Concepts**

Object-oriented programming is a programming paradigm that revolves around the concept of objects, which are instances of classes. OOP promotes concepts such as encapsulation, inheritance, and polymorphism, enabling developers to create modular, reusable, and maintainable code.

**1.2 Overview of Classes in C#**

In C#, a class is a blueprint for creating objects. It defines the structure and behavior of objects by specifying fields, properties, methods, and events. Classes provide a way to model entities with attributes and behaviors, making them powerful tools for organizing and managing complex systems.

**1.3 Importance of Defining Classes in Software Development**

Defining classes is crucial in software development for several reasons:
- Encapsulation: Classes encapsulate data and behavior, hiding the internal implementation details from the outside world.
- Reusability: Classes allow you to create reusable components that can be used across different parts of your application or in other applications.
- Modularity: Classes promote modularity by breaking down complex systems into smaller, manageable units.
- Maintainability: Well-defined classes make code easier to understand, debug, and maintain over time.

---

**Chapter 2: Syntax of Class Declaration in C#**

In this chapter, we'll dive into the syntax of declaring classes in C#. We'll explore how to define fields, properties, methods, constructors, and other members within a class.

**2.1 Syntax of Class Declaration**

```csharp
public class Person
{
    // Fields
    private string name;
    private int age;

    // Properties
    public string Name
    {
        get { return name; }
        set { name = value; }
    }

    public int Age
    {
        get { return age; }
        set { age = value; }
    }

    // Constructor
    public Person(string name, int age)
    {
        this.name = name;
        this.age = age;
    }

    // Method
    public void DisplayInfo()
    {
        Console.WriteLine($"Name: {Name}, Age: {Age}");
    }
}
```

In this example, we define a `Person` class with fields for name and age, properties to encapsulate access to these fields, a constructor to initialize object state, and a method to display information about a person.

**2.2 Creating Objects from Classes**

```csharp
class Program
{
    static void Main(string[] args)
    {
        // Creating objects
        Person person1 = new Person("Alice", 30);
        Person person2 = new Person("Bob", 25);

        // Calling methods
        person1.DisplayInfo();
        person2.DisplayInfo();
    }
}
```

In this example, we create instances of the `Person` class and invoke the `DisplayInfo` method to display information about each person.

---

In this chapter, we've covered the basics of defining classes in C#, including syntax and examples. Classes are fundamental building blocks in C# programming, allowing you to model real-world entities and create modular, reusable, and maintainable code. Stay tuned for more advanced topics on classes in the following chapters!

---

#### 3. Creating Objects
   - 3.1 Instantiating Objects from Classes
   - 3.2 Assigning Values to Object Properties
   - 3.3 Invoking Methods on Objects
   - 3.4 Understanding Object Initialization and Memory Allocation
   - 3.5 Working with Object References and Identity

**Title: C# Fundamentals: Creating Objects**

---

**Chapter 1: Introduction to Creating Objects**

Welcome to the chapter on creating objects in C#! In this chapter, we'll explore the fundamental concepts of object creation in C#, including class instantiation, object initialization, and memory allocation. We'll delve into the syntax and techniques used to create objects from classes and demonstrate various examples to illustrate the process.

**1.1 Understanding Object Creation**

Object creation is a fundamental concept in object-oriented programming (OOP), where objects are instances of classes representing real-world entities or concepts. In C#, objects are created from classes using the `new` keyword, allowing developers to instantiate and manipulate instances of classes at runtime.

**1.2 Overview of Class Instantiation**

Class instantiation is the process of creating objects from classes. When an object is instantiated, memory is allocated for its properties and methods, and the object is initialized to its default state. Each object instance has its own set of properties and methods, independent of other instances created from the same class.

**1.3 Importance of Object Initialization**

Object initialization involves setting initial values for object properties and invoking constructors to perform initialization tasks. Proper object initialization ensures that objects are in a valid and usable state after creation, enabling them to fulfill their intended purpose in the application.

**Chapter 2: Creating Objects from Classes**

In this section, we'll explore how to create objects from classes in C#, including defining classes, instantiating objects, and initializing object properties.

**2.1 Defining Classes**

```csharp
public class Person
{
    public string Name { get; set; }
    public int Age { get; set; }

    public Person(string name, int age)
    {
        Name = name;
        Age = age;
    }

    public void DisplayInfo()
    {
        Console.WriteLine($"Name: {Name}, Age: {Age}");
    }
}
```

In this example, we define a `Person` class with properties for name and age, and a constructor to initialize these properties.

**2.2 Creating Objects**

```csharp
Person person1 = new Person("Alice", 30);
Person person2 = new Person("Bob", 25);
```

Here, we create two `Person` objects, `person1` and `person2`, using the `new` keyword followed by the class constructor.

**2.3 Initializing Object Properties**

```csharp
person1.Name = "Alice";
person1.Age = 30;
```

Alternatively, object properties can be initialized individually after object creation, as shown in this example.

---

In this chapter, we've covered the basics of creating objects in C#, including defining classes, instantiating objects, and initializing object properties. Understanding these concepts is essential for building object-oriented applications in C#. Stay tuned for more advanced topics on object creation and manipulation in the following chapters!

---

#### 4. Class Relationships and Inheritance
   - 4.1 Understanding Class Relationships: Composition vs. Inheritance
   - 4.2 Implementing Inheritance Hierarchies in C#
   - 4.3 Overriding Methods and Properties in Derived Classes
   - 4.4 Using Base Class Constructors and Initialization
   - 4.5 Exploring Polymorphism and Method Overriding

#### 5. Encapsulation and Information Hiding
   - 5.1 Understanding Encapsulation Principles
   - 5.2 Using Access Modifiers to Control Access to Class Members
   - 5.3 Implementing Properties with Getters and Setters
   - 5.4 Applying Encapsulation Techniques for Data Protection

#### 6. Class Design Best Practices
   - 6.1 Writing Clean and Readable Class Definitions
   - 6.2 Applying SOLID Principles for Class Design
   - 6.3 Using Design Patterns to Solve Common Design Problems
   - 6.4 Documenting Classes and APIs for Clarity and Usability

#### 7. Advanced Topics in Classes and Objects
   - 7.1 Implementing Static Members and Static Classes
   - 7.2 Exploring Nested Classes and Inner Classes
   - 7.3 Working with Partial Classes for Code Organization
   - 7.4 Utilizing Object Initialization Syntax and Object Initializers

#### 8. Object Lifecycle Management
   - 8.1 Understanding Object Lifecycle: Creation, Usage, and Destruction
   - 8.2 Managing Object Lifetimes with Garbage Collection
   - 8.3 Implementing IDisposable Interface for Resource Cleanup
   - 8.4 Handling Object Finalization and Clean-Up Operations

#### 9. Conclusion
   - 9.1 Summary of Key Concepts Covered
   - 9.2 Practical Applications of Classes and Objects in C#
   - 9.3 Resources for Further Learning and Exploration

### End of Chapter