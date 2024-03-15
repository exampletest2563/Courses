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