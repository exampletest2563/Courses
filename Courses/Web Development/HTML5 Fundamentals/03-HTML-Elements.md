# 🌱 HTML Elements

## 📢 HTML Headings

`HTML` headings (`<h1>` to `<h6>`) are used to define headings or titles for different sections. These tags represent a hierarchy (levels of significance), where `<h1>` is the main heading (or the most important heading), and `<h6>` is the least significant heading (the least important heading).

```html
<!DOCTYPE html>
<html>
<head>
	<title>HTML Headings</title>
</head>
<body>
	<h1>Main Heading</h1>
	<h2>Sub Heading 2</h2>
	<h3>Sub Heading 3</h3>
	<h4>Sub Heading 4</h4>
	<h5>Sub Heading 5</h5>
	<h6>Sub Heading 6</h6>
</body>
</html>
```

```html
<!DOCTYPE html>
<html>
<head>
	<title>HTML Headings</title>
</head>
<body>
	<h1>Main Heading</h1>
	<p>Some introductory text.</p>
	<h2>Subheading 1</h2>
	<p>Text for the first subheading.</p>
	<h2>Subheading 2</h2>
	<p>Text for the second subheading.</p>
</body>
</html>
```

Headings are crucial for organizing and structuring the content. Correct structure does matter. Search engines and other user agents usually index page content based on heading elements.

In general, an article should have one `<h1>` element for the main title followed by `<h2>` subtitles. If there are `<h1>` elements on a higher level they should not be used to describe any lower level content.

## 📰 HTML Paragraphs

`HTML` paragraphs (`<p>`) are used to define and structure text into distinct paragraphs on a `Web page`. Paragraphs provide a clear separation of content, making it easier to read and understand.

```html
<!DOCTYPE html>
<html>
<head>
	<title>HTML Paragraphs</title>
</head>
<body>
	<p>This is a simple HTML paragraph.</p>
	<p>Another paragraph.</p>
</body>
</html>
```

Explanation:
- `<p>`: Represents a paragraph.
- The content inside `<p>` tags is displayed as a separate paragraph.

## 🖨️ HTML Text Formatting

|HTML Tag|Purpose|
|-|-|
|`<br>`|Bold text|
|`<strong>`|Important text|
|`<i>`|Italic text|
|`<em>`|Emphasized text|
|`<mark>`|Marked text|
|`<small>`|Smaller text|
|`<del>`|Deleted text|
|`<ins>`|Inserted text|
|`<sub>`|Subscript text|
|`<sup>`|Superscript text|
|`<pre>`|Preformatted text|
|`<blockquote>`|Quotations|
|`<q>`|Short quotations|
|`<code>`|Computer code|

## 📜 HTML Lists

`HTML` provides three types of lists: ordered lists (`<ol>`), unordered lists (`<ul>`) and description lists (`<dl>`). Ordered lists are used for items with a specific order, while unordered lists are used for items without a specific order.

```html
<!DOCTYPE html>
<html>
<head>
	<title>HTML Lists</title>
</head>
<body>
	<h2>Ordered List:</h2>
	<ol>
		<li>First Item</li>
		<li>Second Item</li>
		<li>Third Item</li>
	</ol>

	<h2>Unordered List:</h2>
	<ul>
		<li>Home</li>
		<li>Categories</li>
		<li>Contact Us</li>
		<li>FAQ</li>
	</ul>
</body>
</html>
```

Explanation:
- `<ol>`: Represents an ordered list.
- `<ul>`: Represents an unordered list.
- `<li>`: Represents a list item.

We can also nest lists to represent more complex structures.

```html
<!DOCTYPE html>
<html>
<head>
	<title>HTML Lists</title>
</head>
<body>
	<h2>Ordered List:</h2>
	<ol>
		<li>Item 1</li>
		<li>Item 2
			<ol>
				<li>Item 2.1</li>
				<li>Item 2.2</li>
				<li>Item 2.3</li>
			</ol>
		</li>
		<li>Item 3</li>
	</ol>

	<h2>Unordered List:</h2>
	<ul>
		<li>Colors
			<ul>
				<li>Red</li>
				<li>Green</li>
				<li>Blue</li>
			</ul>
		</li>
		<li>Fonts
			<ul>
				<li>Montserrat</li>
				<li>PT Mono</li>
				<li>Monaco</li>
			</ul>
		</li>
	</ul>
</body>
</html>
```

```html
<!DOCTYPE html>
<html>
<head>
</head>
<body>
	<dl>
		<dt>Coffee</dt>
		<dd>Black Hot Drink</dd>
		<dt>Milk</dt>
		<dd>White Cold Drink</dd>
	</dl>
</body>
</html>
```

Explanation:
- `<dl>`: Represents a description list.
- `<dt>`: Represents a description term.
- `<dd>`: Represents a description detail.

`HTML` lists are used for structuring content.

## 🍻 HTML Div & Span Elements

## ➡️ HTML Inline Styles

## 🏕️ HTML Style Tag

## 🛍️ HTML Common Attributes

`HTML` common attributes are attributes that can be applied to almost all `HTML` elements. These attributes provide additional information about elements or control their behavior.

`HTML` common attributes include: `class`, `id`, `style`, `title`, `name` and `lang`. These attributes add extra information to elements and are applied similarly across different tags.

## Metadata