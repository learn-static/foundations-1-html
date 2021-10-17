# Example HTML Document

To understand the basic elements and concepts of HTML, let's review a very basic example HTML document. 
In the "example" folder, take a look at the file ["index.html"](example/index.html).

## Basic Structure 

A most basic HTML page structure might look like:

```
<!DOCTYPE html>
<html>
    <head>
        <title>Hello World!</title>
    </head>
    <body>
        <h1>Hello World!</h1>
        <p>gh-pages is great.</p>
    </body>
</html>
```

Indentation is a convention to make HTML code easier to read. 
It can help you quickly identify how the elements are nested. 
However, web browsers do not care! 
All extra white space and line breaks are ignored when rendering.

### Root Element

Every HTML file starts with the **doctype declaration** which tells your web browser what type of file to expect:

`<!DOCTYPE html>`

After the doctype, the first tag of every web page is the **root element** `<html>`.
The rest of the content is **nested** inside the root element, so the final tag on every HTML file will be `</html>`.

### Head and Body Elements

Inside the root there is generally two main elements that contain the rest of the page content. 

First comes the `<head>` element. 
This section is *not directly displayed* on the web page, but contains information about the page. 
Tags in the head often represent metadata, links to style sheets, or other technical markup that needs to be communicated to the browser.

Second comes the `<body>` element. 
The body is displayed, representing the content of the web page.

### Content Elements

- headings
- paragraphs
- image, `<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/Cat_poster_1.jpg/640px-Cat_poster_1.jpg" alt="six different cats">`
- inline elements, `<strong>bold</strong>` and `<em>italic</em>`
- hyperlink, `<a href="about.html">About page</a>`
- comment, `<!-- not displayed -->`
