# Complete Web Page

A web page is usually more than just HTML. 
The next steps are to add CSS to control the presentation style and JS to provide interactive functionality. 

------------

## CSS

HTML provides content marked up with the semantic structure of the document. 
Cascading Style Sheets is a language that provides the means to style and control the *presentation* of this content in the web browser.
Importantly, this separation of content and presentation gives web pages great flexibility to fluidly adapt to different themes (dark mode), devices (phones), or mediums (print).

CSS is written as a **selector** that targets a specific element on web page and a **property** that sets style rules for that element.
Property values end with a semicolon and are surrounded by curly braces.

`selector { property: value; }`

CSS is **cascading** because the style of each element is calculated following a hierarchy of specificity of each rule that applies.
CSS properties can be written as **inline attributes**, **internal style tags**, or in **external files**.

The examples below will give you a basic idea of how CSS works with your HTML file--for more details about the syntax and options, check an in-depth tutorial such as [W3Schools CCS Tutorial](https://www.w3schools.com/css/default.asp).

### Inline Style Attribute

The most basic way to add CSS to an element is using an attribute on the tag itself.
This is the most specific possible rule, so will over ride other CSS in Internal or External sources.

`<p style="color: red;">Red text</p>`

`<p style="text-align: right; color: green;">Right green text.</p>`

Inline styles are *much* harder to write, maintain, and update than centralizing your CSS, so should be avoided in most cases.
They also render slower in the browser!

### Style Tag

The `<style>` element can be added to the `<head>` of your HTML file to centralize CSS rules for the page.
First, we need **selectors** that will target the correct subset of elements.
Generally, we use **id** and **class** attributes or tag names.

First, add some id's and class's to your HTML file so we can test cascading selectors in action:

```
<p>Grey</p>
<p class="warning">Blue</p>
<p id="alert" class="blue">Blue</p>
```

Now in the `<head>` of your HTML add a `<style>` element:

```
<style>
    #alert { color: yellow; }
    .warning { color: blue; }
    p { color: grey; }
</style>
```

### External CSS 

In practice most CSS is written into an external file that is loaded by the HTML document.
This allows you to create a central location for all the CSS rules that will style all the pages of your website, enabling a consistent and easy to maintain theme.

To load the external CSS, add a `<link>` element to the `<head>` of your HTML file.

`<link rel="stylesheet" href="main.css" type="text/css">`

This external file is often a standard framework created by someone else and may be hosted in a different location than your own site.
For example, the very popular [Bootstrap](https://getbootstrap.com/) on a content delivery network (CDN):

`<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">`

External style sheets loaded further down the HTML file will over ride ones loaded earlier.

-----------

## JS

JavaScript is a programming language originally designed for interacting with HTML in the web browser
(note: it is *not* related to [Java](https://go.java/index.html)).
JS has evolved into a powerful, multipurpose language that enables advanced interactivity and data processing on the **client-side**, i.e. in your web browser rather than on the server.

Similar to CSS, JS can be written inline, in a script tag, or in an external file.
The examples below will give you a basic idea of how JS works with HTML--since JS is a fully featured programming language, to learn more you will need to follow an in-depth tutorial such as [W3Schools JS Tutorial](https://www.w3schools.com/js/default.asp).

### Inline JS Attributes

Add an input button with the JS "onclick" attribute:

`<button type="button" onclick="document.getElementById('alert').innerHTML = 'Hello!'">Inline JS</button>`

Adding JS inline is simple, but has the same draw backs as inline CSS, mixing HTML semantic content with the visual presentation.

### Script Tag

JS contained in a `<script>` element will be executed in order as the HTML loads.
Unless they are critical to immediate presentation, scripts are usually added at the bottom of the HTML file to optimize load times.

Let's add another button:

`<button type="button" id="pop">Pop Up</button>`

Then attach a JS function to the button using a script tag:

```
<script>
    /* set variables */
    var btn = document.getElementById('pop');
    var message = "Hello World!";
    /* create a function */
    function myAlert () {
        alert(message);
    }
    /* add event listener to element */
    btn.addEventListener("click", myAlert);
</script>
```

### External Files

As with CSS, JS will often be contained in a separate file that is loaded by the HTML document. 
Add a `src` attribute to a script tag to load JS:

`<script src="example.js"></script>`

Often, this will be external libraries that simplify adding advanced features to your site.
For example, Bootstrap provides a bundle to add functionality to their pre-built components:

```
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>
```

Now, with Bootstrap CSS and JS bundle being loaded on our HTML file, try adding a [Modal feature](https://getbootstrap.com/docs/5.1/components/modal/):

```
<!-- Button trigger modal -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
  Click Me!
</button>

<!-- Modal -->
<div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel">This is a Modal</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        A Bootstrap Modal!
      </div>
    </div>
  </div>
</div>

```

Notice that we didn't have to write any JS to add the Modal example. 
Bootstrap's library takes care of it all if you follow the mark up pattern (basically by adding the `data-bs-target` attribute).

To debug JS, be sure to open your browser's dev tools and look at the **Console**. 
Any error messages will appear there! 
You can also use `console.log()` to send debug messages from your script.
