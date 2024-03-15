# 🔗 HTML Linking Resources

## 📪 Absolute & Relative Paths

## ⚓ HTML Hyperlinks

Hyperlinks in `HTML` are used to navigate between `Web` pages or link to external resources.

The `<a>` (`anchor`) element is used to create hyperlinks. The `href` attribute specifies the destination of the link, which can be an absolute or relative path / URL.

## 🏞️ HTML Images

The `<img>` tag is used to embed images in `HTML`. The `src` attribute specifies the source (URL or file path) of the image.

```html
<!DOCTYPE html>
<html>
<head>
	<title>HTML Images</title>
</head>
<body>
	<img src="example.jpg" alt="A Beautiful Image" />
</body>
</html>
```

Explanation:
- `<img src="example.jpg">`: Embeds an image with the filename "example.jpg" (assumes the image is in the same directory as the `HTML` file).
- `alt="A Beautiful Image"`: Provides alternative text for accessibility and displays if the image cannot be loaded.

We can turn images into clickable links by wrapping the `<img>` tag with an `<a>` tag.

```html
<!DOCTYPE html>
<html>
<head>
	<title>HTML Image Link</title>
</head>
<body>
	<a href="https://example.com">
		<img src="example.jpg" alt="A Beautiful Image" />
	</a>
</body>
</html>
```

Explanation:
- `<a href="https://example.com">`: Wraps the image in a hyperlink leading to the specified URL.

## 🪅 Favicon

A favicon is a small icon that represents a website and is typically displayed in the browser's address bar, tabs, and bookmarks. Usually, favicons are small square images (16x16 pixels or 32x32 pixels).

The `<link>` element in the `<head>` section of the `HTML` files is used to create a link to the favicon.

```html
<!DOCTYPE html>
<html>
<head>
	<title>Favicon</title>
	<link rel="icon" href="favicon.jpg" type="image/x-icon">
</head>
<body>
	<h1>Welcome to My Website</h1>
	<p>This is a simple HTML document with a favicon.</p>
</body>
</html>
```

Explanation:
- `<link rel="icon" href="favicon.jpg" type="image/x-icon">`: Links to the favicon file, specifying the type as `image/x-icon`.

Adding a favicon to a website enhances its branding and provides a recognizable icon for users.

## 📃 Linking CSS Files

## 📃 Linking JavaScript Files

// TODO: Add defer attribute.

## Embedding Content

## 🪞 IFrames

## 📜 Guides

Place CSS in an external stylesheet for maintainability.

Include JavaScript at the end of the `HTML` body or use the `defer` attribute.