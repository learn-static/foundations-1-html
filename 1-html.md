# Hypertext Markup Language

> This section introduces the concepts behind the markup language HTML.

HTML is a ["markup language"](https://en.wikipedia.org/wiki/Markup_language) originally designed to describe structured documents for the web.

If you look at the pages of a book or the print out of your term paper, you will see a set of common conventions that we use to communicate structure and meaning.
Document features such as headings, paragraphs, lists, or italics are represented on the page by distinctive styling such as font size, boldness, or font decoration.

HTML provides a way to formally mark those types of document elements, allowing you to record the semantic structure of the text.
This markup can then be translated by the web browser into visual styles for easy reading, or efficiently navigated by screen readers for non-visual users.

Of course, as web pages become ever more complicated, HTML has gone far beyond a simple document language!

## HTML Elements

HTML is made up of a set of standard **elements** used to structure a web page and introduce features such as images.
Elements are like annotations describing how chunks of page content should be interpreted by the browser.

HTML elements follow this pattern:

`<tag attribute="value">content annotated by the element</tag>`

- Elements are represented by **tags** enclosed by pointy brackets that usually come in pairs, an opening `<tag>` and closing `</tag>`.
- Elements may have **attributes** inside the brackets that add additional data or qualifications to the tag.
- Elements may enclose content or other elements which are **nested** between the opening and closing tag. The content between the tags is considered described (marked up) by the element.

Note the elements themselves are not displayed by a web browser, but are used as instructions for rendering the content they annotate.

### For Example

For example, in HTML the heading above that says "For Example" looks like:

`<h3>For Example</h3>`

The `<h3>` tag encloses the text "For Example", marking it semantically as a "third level heading" in the document.
The web browser interprets that markup and displays "For Example" differently than the main paragraph text and the `h1` header "Hypertext Markup Language" at the top of this page, to convey it's semantic meaning to readers.

## Next Steps

There are hundreds of elements in the [HTML Living Standard](https://html.spec.whatwg.org/).
However, you will only need to recognize a handful and understand the basic concept of tagging to decipher most pages or write your own.
You shouldn't try to learn HTML by reading the standard! 

Learn more by following the [Examples in the next lesson](2-example.md)!

Practice writing basic HTML via tutorials, inspect live pages to learn from the websites you enjoy, and look up elements in reference sources when you need to remember how they work.
Here are some good options to get started:

- [W3Schools HTML tutorial](https://www.w3schools.com/html/default.asp) provides interactive learning of basic concepts. W3Schools also provides tutorials and reference resources for other web essentials, such as CSS and JavaScript, as well as the free basic hosting service [Spaces](https://www.w3schools.com/spaces/) that is perfect for learning. 
- [MDN Web Docs](https://developer.mozilla.org/en-US/) provides high quality reference and in-depth learning guides.

P.S. Keep in mind that on the live web you will see a lot of *badly written* HTML!
Although HTML is technically a strict standard, web browsers are *very forgiving*. 
They will display markup that breaks all the rules.
