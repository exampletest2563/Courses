# 📜 History Of The Web

## 🌍 Internet & World Wide Web

In 1989, Tim Berners-Lee, a British computer scientist, proposed the concept of a `decentralized information system` that would eventually become the `World Wide Web` (`WWW`). His vision included the use of `hypertext` to link documents and a system of `uniform resource identifiers` to uniquely identify resources.

In 1990, Tim Berners-Lee implemented the first successful communication between a `Hypertext Transfer Protocol` (`HTTP`) client and server, effectively creating the foundation for the `Web`. The first website, `info.cern.ch`, and the first web browser, `WorldWideWeb` (later renamed `Nexus`), were developed in 1991.

There is a difference between `Internet` and `Web` as `Internet` refers to a network of networks that connects devices all over the world, while `Web` is an information system that enables information sharing over the `Internet`.

The Internet is like a global network of interconnected computers, while the World Wide Web is the system of information and resources accessible via the Internet.

## 🤔 Web Page, Website & Web Application

A `Web page` is a single document that can be accessed through a `Web browser`. It contains text, images, and links. It is usually written in `HTML`, and it represents the basic unit of information on the `Web`. Examples: A blog post, an article, or a product detail page on an e-Commerce `Website`.

```html
<!DOCTYPE html>
<html>
<head>
	<title>My First Web Page</title>
</head>
<body>
	<h1>Hello World!</h1>
	<p>This is my first Web page.</p>
</body>
</html>
```

A `Website` is a collection of related `Web pages` grouped together under a common `domain` or `subdomain`. Normally, a `Website` consists of multiple interconnected `Web pages`. `Websites` need to have consistent theme or design across pages. Navigational elements (`menus`, `links`) help users move between `Web pages`. Examples: An online encyclopedia like Wikipedia, a news `Website`, or an e-Commerce platform.

A `Web Application` (or `Web App`) is a dynamic and interactive software program accessible through a `Web Browser`. `Web Applications` offer functionality beyond displaying information (e.g., user input, data processing). Examples: Social media platforms (e.g., Facebook), email services (e.g., Gmail), or online productivity tools (e.g., Google Docs).

|Key Differences|Web Page|Website|Web Application|
|-|-|-|-|
|Interactivity|Primarily static, displaying information.|Can have dynamic elements, but the focus is on presenting information.|Highly interactive, allowing users to perform actions and manipulate data.|
|Functionality|Limited functionality, typically informational.|More functionality than a single page, but may not offer complex interactions.|Provides advanced functionality, often resembling desktop applications.|
|User Experience|Simple navigation, minimal user interaction.|Navigational structure for exploring related content.|Rich user interface.|
|Example|About Us page.|E-Commerce site with multiple product pages.|Online project management tool.|

## 🚀 HTML, CSS & JavaScript

`HTML` (HyperText Markup Language) is used to define `the content` of Web pages. It uses elements, tags and attributes to define building blocks/components such as `headings`, `paragraphs`, `images`, `links`, and more.

`HTML Example`

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Document</title>
		<meta charset="UTF-8">
	</head>
	<body>
		<h1>HTML Introduction</h1>
	    <p>This is a basic HTML document.</p>
	</body>
</html>
```

`CSS` (Cascading Style Sheets) is used to specify `the layout` of Web pages. `CSS` is responsible for styling HTML elements, controlling `layout`, `design`, and `presentation`. `CSS` was introduced to separate the presentation of Web documents from their structure.

`CSS Example`

```css
body {
	font-family: 'Arial';
	background-color: white;
}

h1 {
	color: black;
	text-align: center;
}

p {
	font-size: 14px;
}
```

`JavaScript` is used to program `the behavior` of Web pages (client-side interactivity), significantly enhancing the user experience.

`JavaScript Example`

```js
document.getElementById("demo").style.visibility = "hidden";
```

`HTML` is mainly used for organization of Web page content, `CSS` is used for definition of content presentation style, and `JS` defines how the content interacts and behaves with the user. Historically, this was not the case: prior to the introduction of `CSS`, `HTML` performed both duties of defining semantics and style.

`Separation of Concerns` is a design principle for separating a computer program into distinct sections. Each section addresses a separate concern, a set of information that affects the code of a computer program.

## 🏕️ Front-End & Back-End

`Front-end development`, or `client-side development`, focuses on the `user interface and user experience` of a website. It involves crafting the `visual elements`, `layouts`, and `interactivity` that users interact with directly.

Technologies:
- Languages: `HTML`, `CSS`, `JavaScript`;
- Frameworks / Libraries: `React`, `Angular`, `Vue.js`.

Front-end developers often utilize frameworks and libraries like `React`, `Angular`, or `Vue.js` to streamline development, manage state, and create modular and reusable components.

`Back-end development`, or `server-side development`, focuses on `server operations` (requests & responses), `database management`, and `application / business logic`. It ensures `data processing, storage, and retrieval`, as well as `handling business logic` that powers the application. Example: How user data is stored? How login / authentication works? What happens when a form is submitted?

Technologies & Languages: `Node.js`, `Python`, `PHP`, `Java`, `C#`.

Front-end and back-end communicate via the `Hypertext Transfer Protocol` (HTTP). The front-end sends requests, and the back-end responds with data or performs actions.

`Full-stack development` includes both front-end and back-end development.

## ⚙️ Client-Server Architecture

Client-Server Architecture is a networked computing model where client devices request services or resources from centralized servers. This separation of concerns enhances scalability, maintenance, and resource management.

The client is the end-user device or application that initiates requests for services or resources. Examples include web browsers, mobile applications, and desktop applications.

The server is a centralized system that processes client requests, performs necessary computations, and manages data. Servers can specialize in various tasks, such as web servers, database servers, or application servers.

Client and server communication is typically established through protocols like `HTTP` (HyperText Transfer Protocol) for Web applications. Clients send requests to servers, and servers respond with the requested data or perform actions.

Request-Response Cycle while browsing a website:
- You (Client): Type a website address (e.g., www.example.com) into your browser.
- Your Device (Client): Sends a request to the server hosting www.example.com.
- Server: Processes the request, retrieves the `Web page`, and sends it back to your browser.
- You (Client): See the `Web page` on your screen.

## 🕵️‍♂️ User-Agent String

The `User-Agent string` is an `HTTP header field` that browsers send to servers to identify themselves. It includes details about the browser, operating system, and sometimes additional information about the device.

It's a small piece of text that tells websites what kind of browser and operating system you're using.

A typical User-Agent string consists of the following components:
- `Browser Information`: Specifies the name and version of the browser.
- `Operating System`: Indicates the operating system running on the client device.
- `Device Information`: In some cases, details about the device, such as model or form factor.

`Example`

```
Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.124 Safari/537.36
```

In this example:
- `Mozilla/5.0`: Represents compatibility.
- `(Windows NT 10.0; Win64; x64)`: Indicates the Windows 10 operating system and 64-bit architecture.
- `AppleWebKit/537.36 (KHTML, like Gecko)`: Denotes the browser engine.
- `Chrome/91.0.4472.124`: Specifies the Chrome browser version.
- `Safari/537.36`: Highlights compatibility with the Safari browser.

Websites use your User-Agent to give you the best experience.

## 🌐 Browsers

Browsers are software applications that allow us to access and interact with information on the World Wide Web.

The main components of a browser include a User Interface and a Rendering Engine. The User Interface includes buttons, an address bar, and menus we interact with. The Rendering Engine interprets and displays `Web` content, converting code into the visual `Web pages` we see.

Rendering Engines: `Blink` (Chrome & Edge), `Gecko` (Firefox), `WebKit` (Safari), `Presto` (Old Opera).

Differences between browsers include:
- Rendering Engine;
- Speed;
- Privacy (Firefox, for instance, emphasizes user privacy);
- Integration (Safari seamlessly integrates with Apple devices);
- Customization (Firefox allows extensive customization);
- Developer Tools.

The late `1990s` and early `2000s` saw intense competition among `Web Browsers`, known as the `Browser Wars`. Internet Explorer, Netscape Navigator, and later Firefox, Chrome, Safari, and Opera battled for dominance. During the height of the `Browser Wars`, developers often implemented features specific to a certain `Web Browser`, leading to compatibility challenges. Later, organizations like the World Wide Web Consortium (W3C) aim to establish and maintain `Web standards`, reducing the compatibility issues for developers.