# 🔣 Operators Overloading

`Complex.cs`

```csharp
public class Complex
{
	public double Real { get; set; }

	public double Imaginary { get; set; }

	public static Complex operator +(Complex x, Complex y)
	{
		return new Complex
		{
			Real = x.Real + y.Real,
			Imaginary = x.Imaginary + y.Imaginary
		};
	}

	public override string ToString()
	{
		// TODO
	}
}
```

`Startup.cs`

```csharp
public class Startup
{
	public static void Main()
	{
		var a = new Complex()
		{
			Real = 1,
			Imaginary = 2
		};

		var b = new Complex()
		{
			Real = 4,
			Imaginary = 8
		};

		var c = a + b;
		Console.WriteLine(c);
	}
}
```