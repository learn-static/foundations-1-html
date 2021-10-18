# The Web

The content of the world wide web is made up of three parts:

- **HTML** (Hypertext Markup Language) provides the structure and content
- **CSS** (Cascading Style Sheets) provides the style
- **JS** (JavaScript) provides the interactivity

When you access a website the owner's server sends your computer the code (written in HTML, CSS, and JS) which your browser then renders into a web page that you can view and interact with.

## View Source 

**Right click** on any web page and select "**View page source**" from the context menu to see the code that is being rendered by your browser (shortcut: `Ctrl + U`). 

Or put `view-source:` in front of any URL in your address bar, for example:

`view-source:https://evanwill.github.io/web-crash-course/`

This is HTML!
(We'll learn more in the next lesson, but just take a peak now)

On another web page, right click on any element in the page and select "Inspect" or "Inspect Element" from the context menu to open your browser's built in **developer tools**. 
Dev tools let you look at the code in context, which can be a great way to learn about HTML and to understand how others created the sites you use.

## Uniform Resource Locators

To retrieve that code we need a web address. 

The links in your browser's address bar are Uniform Resource Locators, **URLs**.
These are basically identifiers used to ask servers for specific pages or content. 
We send a request with information to the server, it sends us a response (hopefully the page we want!).

An example URL might look like:

`https://sub.example.com/about.html?key=value#anchor`

We can dissect this URL into these component parts:

protocol `://` subdomain `.` domain `.` top-level domain `/` path and filename `?` query with parameters `#` anchor

Each component of the URL plays a part in what is eventually displayed in your browser, so it is helpful to understand the pieces:

- **Protocol:** there is more than 100 defined Internet Protocols, however with URLs the most common is [Hypertext Transfer Protocol (HTTP)](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol), i.e. `http://` or `https://`. So your URL starts there!
- **Subdomain, Domain, and Top-Level Domain:** the [Domain Name System (DNS)](https://en.wikipedia.org/wiki/Domain_Name_System) is often described as a "phone book" that translates easy to understand web addresses into the appropriate [IP addresses](https://en.wikipedia.org/wiki/IP_address) of servers with the desired information. This is the heart of the URL, basically the website's name that points to a computer connected to the internet (i.e. a server). A subdomain is an optional prefix of the domain designating a subsection of the site. The top-level domain is the suffix, e.g. `.com`, `.org`, or `.pizza`. For example, in "lib.uidaho.edu", `lib` is the subdomain (the university library) of `uidaho` (the university), which is a subdomain of the top-level domain `edu`. 
- **Path and filename:** these can be imagined like folders and files located on the server. For example, `/about/dogs.html`, is the file "dogs.html" in the "about" folder. If no filename is given, by default the server provides the file named `index`.
- **Query:** an optional string added to the end of the address following a `?`. The query string is given in key value pairs like `key=value`. Multiple pairs can be separated by `&`. The queries are processed by the server or javascript, so what exactly they do depends on the page. For example, `/index.php?title=example&action=edit` might return a wiki article in edit mode from a server running PHP.
- **Anchor:** an optional string added to the end of the address following a `#`. Anchors traditionally correspond to specific element `id` on an HTML page (like an internal link to content, rather than a link to an external page), but are often used by javascript to add other functionality. For example, `/index.html#Chapter1` might jump to a chapter heading in the web page, or `/about.html#help` might pop up a modal.

## 404?

When you send a request to a server (i.e. type in an address, click on a link, or fill in a form) it sends back a status code to let your browser know what is happening. 
Users generally don't see the status codes, except the dreaded 404. 

404 is an error message in the HTTP protocol, saying that the URL doesn't correspond to anything on the server, i.e. the page can't be found, there is nothing at that address!
Most websites have a special page that displays when you get a 404.

## More 

To start understanding and developing websites you honestly don't need to know much about how the web works.
Familiarize your self URLs, learn a bit about HTML, and you are already understanding the fundamentals of the web!

Learn about [HTML in the next lesson](1-html.md).

For more background about how the web works:

- [How Does the Internet Work?](https://youtu.be/i5oe63pOhLI) (idealistic Canadian video explains that *The internet is network of networks that connects devices.*)
- Julia Evan's [Networking Zine](https://wizardzines.com/zines/networking/)
