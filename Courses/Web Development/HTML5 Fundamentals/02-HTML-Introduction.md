# 🔥 HTML Introduction

## 📌 HyperText Markup Language

`HTML` (HyperText Markup Language) is the standard markup language for creating `Web pages`. `HTML` uses a markup system composed of elements which represent specific content.

// TODO: Web Standard

The word `hypertext` refers to text that:
- contains links (`hyperlinks`) to other documents or resources;
- transfer information on the `Web`.

`HTML` provides a structured and standardized way to organize content on `Web pages`.

`HTML` is sometimes called a programming language but it has no logic, so is a `markup language`.

`HTML` uses tags (enclosed in angle brackets) to define the structure and elements of a documents. These tags represent the structure, the meaning and the importance of the content.

A `HTML` page may consist of potentially hundreds of elements which are then read by a `Web` browser, interpreted and rendered into human readable or audible content on the screen.

## 📜 HTML Documents

`HTML` documents are files with `.html` extension.

```html
<!DOCTYPE html>
<html>
<head>
	<title>My First HTML Document</title>
</head>
<body>
	<h1>Welcome to My Website!</h1>
	<p>This is my first HTML document.</p>
</body>
</html>
```

Steps to create a `HTML` document:
1. Copy the `HTML` code.
2. Open a text editor (like Notepad, Notepad++ or Visual Studio Code).
3. Paste the code and save the file with a `.html` extension. Normally, `HTML` files are named `index.html`.
4. Double-click the file to open it in your default `Web` browser.

Editing the contents of the `HTML` document involves saving the changes and refreshing the browser page.

In order to edit the contents of the `HTML` document:
1. Save the changes.
2. Refresh the page in your browser.

## 💭 HTML Comments

`HTML` comments are annotations within the `HTML` code that are not displayed when the `Web page` is viewed in a browser. They are useful for leaving notes, explanations, or temporarily excluding parts of the code. In other words, comments provide other developers with development specific information without affecting the user interface.

`HTML` comments are initiated with `<!--` and concluded with `-->`.

```html
<!-- This is an HTML comment. -->
<p>This is a paragraph.</p>
```

Explanation:
- `<!--`: Indicates the start of the comment.
- `This is an HTML comment.`: The Comment content.
- `-->`: Indicates the end of the comment.

We can use comments to label or organize code sections.

```html
<!-- Header Section -->
<h1>My Website</h1>

<!-- Main Content Section -->
<p>Welcome to my website!</p>
```

Comments can also span multiple lines to provide more information.

```html
<!--
	This is a multiline HTML comment.
	The browser will not render this text.
-->
```

## 📃 HTML Document Structure

A simple `HTML` document typically consists of two main sections: the `head` and the `body`.

```html
<!DOCTYPE html>
<html>
<head>
	<title>My First HTML Document</title>
</head>
<body>
	<!-- Our Content Goes Here... -->
</body>
</html>
```

Explanation:
- `<!DOCTYPE html>`: Declares the HTML version.
- `<html>`: The root element, containing all other elements.
- `<head>`: Contains meta-information about the document.
- `<title>`: Sets the title of the `Web page` (visible in the browser tab).
- `<body>`: Contains the content of the `Web page`.

```html
<!DOCTYPE html>
<html>
<head>
	<title>My First HTML Document</title>
</head>
<body>
	<h1>Welcome to My Website!</h1>
	<p>This is my first HTML document.</p>
</body>
</html>
```

Explanation:
- `<h1>`: Defines a top-level heading.
- `<p>`: Represents a paragraph.

// TODO: \<head> & \<body> tabulation.

## 🧩 HTML Tags & Elements

// TODO: Head & Body

`HTML` uses tags like `<h1>` and `<p>` to define the structure and the content of a `Web` page.

An `HTML` element consists of an opening tag, content, and a closing tag. Tags are enclosed in angle brackets `< >`.

```html
<p>This is an HTML element.</p>
```

Explanation:
- `<p>`: The opening tag.
- `This is an HTML element.`: The content.
- `</p>`: The closing tag.
- `<p>This is an HTML element.</p>`: The `HTML` element.

`HTML` tags examples:
- `<h1>`: Used to define the main heading.
- `<p>`: Used to define a paragraph.
- `<strong>`: Used to define bold text.
- `<em>`: Used to define italic text.

```html
<!DOCTYPE html>
<html>
<head>
	<title>HTML Elements</title>
</head>
<body>
	<h1>This is a Heading</h1>
	<p>This is a paragraph.</p>
	<p>This is <strong>bold</strong> and this is <em>italic</em>.</p>
</body>
</html>
```

Elements can also be self-closing if they don't have content.

// TODO: \<br/>

## 🛍️ HTML Attributes

`HTML` attributes provide additional information about `HTML` elements. They are always included in the opening tab and come in name/value pairs. Attributes modify the behavior or appearance of an element.

```html
<a href="https://example.com">Visit Example.com</a>
```

Explanation:
- `<a>`: The opening tag for a hyperlink.
- `<href>`: The attribute name.
- `"https://example.com"`: The attribute value.

// TODO: Add width & height with Lorem Ipsum text.

## 🔌 Browsers & Browser Tools

`Web` browsers are software applications that allow us to access and interact with information on the `World Wide Web`. They interpret `HTML`, `CSS`, and `JavaScript` to render `Web` pages.

## 🪄 HTML5

`HTML5` is the latest version of `HTML`.

`HTML5` introduces semantic elements that enhance document structure and accessibility. Examples include: `<header>`, `<nav>`, `<article>`, `<section>`, `<footer>`, and `<main>`.

`HTML5` brings features like native video and audio support.

## ⚔️ Styles & Semantics

`HTML` is all about content and its structure and semantics. Structure dictates the organization and layout, while content provides the substance. Using the right tags in the right places helps browsers and search engines understand the content.

`HTML` provides the basic structure and semantics for `Web` content. It allows developers to organize text, images, links, and other elements into a coherent and visually appealing layout.

Visual representations of the content are defined by Cascading Style Sheets (`CSS`) and realized by browsers.

> Any existing elements that could be used for visual representations within HTML are entirely obsolete and must not be used.

## ✅ HTML Validation

`HTML` validation is the process of checking if a `Web` page's `HTML` code follows the rules and guidelines defined by the `HTML` specification. Validation ensures that the `HTML` code is syntactically correct and adheres to the standards set by the World Wide Web Consortium (W3C).

There are several ways to spot invalid `HTML` code:
- `Online Validators`: We can use `HTML` validators provided by the W3C or other organizations. We can simply copy and paste our `HTML` code into an online validator. Example: https://validator.w3.org.
- `Browser Developer Tools`: Most modern browsers come with built-in developer tools that include `HMTL` validation features. We can monitor the `Console` tab for any `HTML` validation errors or warnings.
- `Integrated Development Environments`: Many code editors have built-in validation features or support plugins / extensions for `HTML` validation.

Common `HTML` validation errors:
- `Unclosed Tags`: All non self-closing elements need to have their corresponding closing tags.
- `Nesting Errors`: All opening and closing tags need to be paired.
- `Invalid Attributes`: All attribute names and values need to be valid for each `HTML` element.
- `Deprecated Elements`: All deprecated `HTML` elements and attributes must not be used.

Validation is a good practice, but minor errors that do not affect rendering or functionality may be acceptable in some cases.