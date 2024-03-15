# Generics

```csharp
public class Box<T>
{
	public static IList<T> data;

	public Box()
	{
		this.data = new List<T>();
	}

	public void Add(T item)
	{
		this.data.Add(item);
	}

	public IEnumerable<T> Spill()
	{
		// TODO: Randomize the order of the elements
	}
}
```