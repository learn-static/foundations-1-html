# Example HTML Documents

To understand the basic elements and concepts of HTML, let's review a very basic example HTML document. 

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
        <p>This website is great.</p>
    </body>
</html>
```

If you want to practice, open a text editor on your computer, paste in this basic structure, and save it with the filename "index.html".
In the folder where you saved it, double click on the file to open it in your web browser. 
You should see our super basic page rendered!

Try editing the content inside the elements `<title>`, `<h1>`, and  `<p>` to see if you can decipher how they correspond to what is displayed.
Refresh the file displayed in your browser to see the effects.

Below are some more details about the parts of this example.

### Indentation and White Space

Notice how each nested element in the example above is indented from the level of it's parent element.
Indentation is a *convention* to make HTML code easier to read. 
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
For example, the `<title>` tag will display in the browser's title bar / tab title (but not on the page itself).

Second comes the `<body>` element. 
The elements inside the body are displayed, representing the content of the web page.
Our basic example has a `<h1>` (i.e. a heading one) and `<p>` (i.e. a paragraph).

### Content Elements

Try editing the example on your computer to add some additional content to your web page.
Remember to refresh your browser as you edit the file to view the results!

- Headings - help denote titles of sections and subsections of a page. They run from `<h1>` through `<h6>`, with hierarchical importance something like what you might see in a traditional table of contents.
- Paragraphs - `<p>` denote blocks of text to be displayed.
- Inline elements - try adding `<strong>bold</strong>` and `<em>italic</em>` to text inside of your paragraphs.
- Hyperlink - links are central to the web, try adding on following the pattern `<a href="https://example.com">hyperlink text</a>`. Notice that the `a` tag uses the attribute `href` with the value being the URL you want to link to. Since the `href` is inside the pointing brackets, it isn't displayed on the page. When you click the hyperlinked text, the browser will navigate to the the `href`.
- Image - try adding an image tag `<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/Cat_poster_1.jpg/640px-Cat_poster_1.jpg" alt="six different cats">`. Notice the `img` tag makes uses of two attributes, `src` (i.e. the link to the image file) and `alt` (i.e. text describing the image content to display if the image can't be).

Your final file might look like:

```
<!DOCTYPE html>
<html>
    <head>
        <title>Hello World!</title>
    </head>
    <body>

        <h1>Hello World!</h1>
        <p>This website is great.</p>

        <h2>Heading Two</h2>
        <p>Another interesting bit of content with some <strong>bold</strong> and <em>italic</em> text.</p>
        <p>Maybe you would like to visit <a href="https://github.com/learn-static">Learn-STATIC</a>?</p>
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/Cat_poster_1.jpg/640px-Cat_poster_1.jpg" alt="six different cats">

    </body>
</html>
```

## More

This example walked through basic HTML elements. 
However, they are currently unstyled!
Next step is to control the presentation using CSS.
