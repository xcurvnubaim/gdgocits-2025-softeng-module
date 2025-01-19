<div align=center>

# Introduction to Web Development

</div>

## Table of Contents
- [1. Introduction](#introduction)
- [2. Web Development Tools](#2-web-development-tools)
- [3. HTML (HyperText Markup Language)](#3-html-hypertext-markup-language)
- [4. CSS (Cascading Style Sheets)](#4-css-cascading-style-sheets)

## 1. Introduction

### How Website Works ?
Computers connected to the internet are called clients and servers. A simplified diagram of how they interact might look like this:

![alt text](image-1.png)

Clients are the typical web user's internet-connected devices (for example, your computer connected to your Wi-Fi, or your phone connected to your mobile network) and web-accessing software available on those devices (usually a web browser like Firefox or Chrome).

Servers are computers that store webpages, sites, or apps. When a client device wants to access a webpage, a copy of the webpage is downloaded from the server onto the client machine to be displayed in the user's web browser.

![alt text](image.png)

1. Every client and server have an ip address on internet
2. When client go to www.example.com, client will create dns query to determine what server ip
3. Client send request to server with ip from dns query
4. Server send response to client, the web browser will render html,css,js file from server

## 2. Web Development Tools
### Web Development Tools:
- **Text Editors / IDE**: [Visual Studio Code](https://code.visualstudio.com/), [Cursor](https://www.cursor.com/), [WebStorm](https://www.jetbrains.com/webstorm/).
- **Browsers**: Chrome, Firefox, Edge.
- **Version Control System**: Git.

### Hosting Providers:
- GitHub Pages, Netlify, Vercel, AWS, etc.

## 3. HTML (HyperText Markup Language)

### What is HTML?
HTML (HyperText Markup Language) is a markup language that tells web browsers how to structure the web pages you visit. It can be as complicated or as simple as the web developer wants it to be. HTML consists of a series of elements, which you use to enclose, wrap, or mark up different parts of content to make it appear or act in a certain way. The enclosing tags can make content into a hyperlink to connect to another page, italicize words, and so on.

### Anatomy of an HTML element
![alt text](image-2.png)
- **The opening tag**: This consists of the name of the element (in this example, p for paragraph), wrapped in opening and closing angle brackets. This opening tag marks where the element begins or starts to take effect. In this example, it precedes the start of the paragraph text.

- **The content**: This is the content of the element. In this example, it is the paragraph text.

- **The closing tag**: This is the same as the opening tag, except that it includes a forward slash before the element name. This marks where the element ends. Failing to include a closing tag is a common beginner error that can produce peculiar results.

### Nesting elements
```html
<p>My cat is <strong>very</strong> grumpy.</p>
```
In the example above, we opened the p element first, then opened the strong element. For proper nesting, we should close the strong element first, before closing the p.

### Void elements
Not all elements follow the pattern of an opening tag, content, and a closing tag. Some elements consist of a single tag, which is typically used to insert/embed something in the document. Such elements are called void elements. For example, the <img> element embeds an image file onto a page:
```html
<img
  src="https://raw.githubusercontent.com/mdn/beginner-html-site/gh-pages/images/firefox-icon.png"
  alt="Firefox icon" />
```

### Basic Structure of an HTML Document
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

**Key Components of the Syntax**

1. `<!DOCTYPE html>` : Declares the document type as HTML5.
2. `<html>` : The root element of the document. The lang="en" attribute specifies the language.
3. `<head>` : Contains metadata (information about the document) like the character set, title, and viewport settings.
4. `<meta>`
    - `charset="UTF-8"` : Ensures the document supports all characters (like emojis, special characters). 
    - `name="viewport"` : Makes the page responsive for mobile devices.
5. `<title>` : Defines the title shown in the browser tab.
6. `<body>` : Contains all visible content, like text, images, and links.

---
More about HTML :

- https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content
- https://developer.mozilla.org/en-US/docs/Web/HTML

## 4. CSS (Cascading Style Sheets)
Cascading Style Sheets (CSS) is a stylesheet language used to describe the presentation of a document written in HTML or XML (including XML dialects such as SVG, MathML or XHTML). CSS describes how elements should be rendered on screen, on paper, in speech, or on other media.

### What is CSS?
Like HTML, CSS is not a programming language. It's not a markup language either. CSS is a style sheet language. CSS is what you use to selectively style HTML elements. 

### Basic CSS Syntax
CSS follows a simple syntax of selectors and declarations.

**Syntax Structure:**
```css
selector {
    property: value;
}
```
- Selector: Targets the HTML element(s) to style.
- Property: Defines the style aspect to modify (e.g., color, font-size).
- Value: Specifies the value for the property.

**Example:**
```css
h1 {
    color: blue;
    font-size: 2em;
    text-align: center;
}
```

### Ways to Add CSS to HTML
1. **Inline CSS**

    CSS directly inside an HTML element using the `style` attribute.
    ```html
    <p style="color: red; font-weight: bold;">This is inline CSS.</p>
    ```

2. **Internal CSS**

    CSS written inside a `<style>` tag within the <head> section of the HTML document.
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Internal CSS</title>
        <style>
            body {
                background-color: lightgray;
            }
            p {
                color: green;
                font-size: 16px;
            }
        </style>
    </head>
    <body>
        <p>This is styled using internal CSS.</p>
    </body>
    </html>
    ```

3. **External CSS**

    CSS written in a separate file and linked to the HTML document.

    `index.html`
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>External CSS</title>
        <link rel="stylesheet" href="styles.css">
    </head>
    <body>
        <p>This is styled using external CSS.</p>
    </body>
    </html>
    ```

    `styles.css`
    ```css
    body {
    background-color: #f0f0f0;
    }
    p {
        color: navy;
        font-family: Arial, sans-serif;
    }
    ```

### CSS Selectors
- **Element Selector**: Targets elements by tag name.

    Example: 
    ```css
    p { color: red; }
    ```
- **Class Selector**: Targets elements by class name

    Example:
    `index.html`
    ```html
    <div class="container">Hello</div>
    ```

    `styles.css`
    ```css
    .container {
        padding: 20px;
        background-color: yellow;
    }
    ```

- **ID Selector**: Targets an element by its unique ID.

    Example:
    `index.html`
    ```html
    <div id="main-content">Content</div>
    ```

    `styles.css`
    ```css
    #main-content {
        font-size: 18px;
        color: black;
    }
    ```

- **Group Selector**: Targets multiple elements

    Example:
    ```css
    h1, p {
        margin: 10px;
    }
    ```

---
More about CSS:

- https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Your_first_website/Styling_the_content
- https://css-tricks.com/
- https://www.w3schools.com/cssref/index.php