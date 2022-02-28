# HTML

-   **HyperText Markup Language (HTML)** is used to create web pages (front end!)
-   A markup language is descriptive not programmatic.
-   HyperText refers to the ability of HTML to easily “link” to other pages.
-   HTML is the standard for displaying webpages on the internet.
-   HTML syntax is broken down into two subsets: elements and attributes.

-   Hyper Text Markup Language
-   Content and structure of a web page
-   HTML is made up of tag/elements
-   These tags can have additional properties called **attributes**
-   **Semantic tags** are HTML elements that describe what they are - p, table, h1, img - non-semantic - div or span (just organization)
    \<h1>Hello</h1>

```html
<h1>Hello Everyone!</h1>

<!-- Self closing tag -->
<img src="something.jpg" alt="" />
```

-   Minimal HTML page

```html
<!DOCTYPE html>
<html>
	<head> </head>
	<body></body>
</html>
```

## Syntax 1.) HTML Elements

-   Elements provide the structure of the document and are defined by tags.
    -   <tagname>content</tagname>
    -   Eg \<div> this is a div element \</div>
-   Like XML, HTML must have its tags properly nested in order to be valid.
    -   Correct: \<div> \<p> \</p> \</div>
    -   Incorrect: \<div> \<p> \</div> \</p>
-   Two categories/types of elements:
-   **Block elements**:
    -   these elements will render as a block on the page meaning any following element will render on a new line by default.
    -   Blocks a line for itself.
-   **Inline elements**:
    -   these can sit next to each other on the same line when rendered.
    -   Can be rendered in the same line as each other.
-   Common HTML Elements:
    -   \<div> defines a “division” of the page. Often contains other elements. (block)
    -   \<h1> through \<h6> are header tags. 1 is the largest 6 is the smallest. (block)
    -   \<p> defines a paragraph (block)
    -   \<span> standard inline element.
    -   \<br> line break (does not need a closing tag) (inline)
    -   \<img> displays an image (does not need closing tag) (inline)
    -   \<a> anchor tag used to make a hyperlink. (inline)

## Syntax 2.) HTML Attributes

-   Attributes are metadata used to describe the elements
    -   you can think of them as parameters defining the specific tag.
-   Attributes are defined within a tag as a key/value pair.
    -   Example: \<img src=”https://cdn.trendhunterstatic.com/thumbs/Tea-Cup-Kittens.jpeg” />
-   Global attributes are those that can be applied to any tag. Some include:
    -   class
    -   id
    -   hidden
    -   lang
    -   style
    -   title

## HTML Doctype Declaration & Root Tag:

-   <!DOCTYPE html>
    -   this is the doctype declaration.
    -   It informs the browser what type of document we are displaying (HTML) as well as the version.
    -   The one above defines a HTML 5 document. THIS IS NOT A TAG!
-   The root tag of an HTML document is \<html>.
    -   Everything must go in between the opening and closing tags of this element.
-   \<head> section for metadata
-   \<body> section for the actual contents to be displayed.

## Document Object Model(DOM)

-   Defines a standard for accessing documents
-   3 Types of DOM:
    -   Core DOM: standard for all document types
    -   XML DOM: standard for XML documents
    -   HTML DOM: Standard for HTML documents
-   **HTML DOM**
    -   standard object medel and programming interface for HTML
    -   Defines:
        -   HTML elements as **objects**
        -   **properties** of all HTML elements
        -   **methods** to access all HTML elements
        -   **events** for all HTML elements
-   This represents the doucment with a logical tree

![DOM](https://www.w3schools.com/js/pic_htmltree.gif)

## HTML Tables:

-   Tables are an easy way to structure our HTML pages and display information.
    -   There was a time when almost all HTML pages were just giant tables.
-   To create a table we begin with a \<table> tag.
    -   \<thead> will define header rows
        -   Inside that we can have the \<tr> which will create an actual row.
        -   \<th> will then give the actual cell data for that header cell.
    -   \<tbody> defines the body of a table.
        -   Each row of the table will have a \<tr> tag.
        -   Individual cells in the row will have a \<td> tag
    -   \<tfoot> can be used to add a footer element to your table.

## HTML Lists:

-   Besides tables, HTML also has built in functionality for displaying lists of items.
-   There are two types of lists: Ordered and Unordered.
    -   **Ordered lists**
        -   have a progression such as 1 2 3… etc
        -   used the \<ol> tag
    -   Unordered list
        -   do not have progression (bullet)
        -   use the \<ul> tag
-   Items in either type of list use the \<li> tag.
-   _Note:_ lists of either type can be nested inside other lists.

## HTML 5 Features:

-   HTML 5 introduced the DOCTYPE declaration.
    -   Also, you can just type ! in a new .html file and it’ll give you skeleton tags
-   Character encoding declaration: \<meta charset=”UTF-8”>
-   Covers pretty much every character in the world

### Semantic Elements

-   HTML 5 added many semantic elements beyond what had already existed.
-   Semantic elements are element tags that are descriptive of the tags intended use beyond just their functionality.
    -   \<section>
    -   \<article>
    -   \<header>
    -   \<footer>
    -   \<summary>
-   Non-semantic tags:
    -   \<div>
    -   \<span>
    -   \<a>
-   HTML 5 also introduced elements to natively embed audio and video.
    -   \<audio> will have an audio element (mp3, ogg, wav are supported) to play on your page.
    -   \<video> will have a video element. (MP4, WebM, ogg are all supported.)
-   HTML 5 also added form validation. See below for notes on forms.

## HTML Forms:

-   HTML has built in functionality for forms.
    -   Forms take various inputs and then submit to a server or handle them with JavaScript etc.
-   Input elements include:
    -   Text field
    -   Password - prevents the inputs from being displayed on the screen.
    -   Radio Buttons - select one from a list of options.
    -   Checkboxes - select multiple from a list of options
    -   Select Boxes - drop down menu to select an option
    -   File select boxes - Allows you to upload a file from your local machine.
    -   Text Area - A multi-line text field.
    -   Reset and Submit buttons.
    -   Attributes used in forms:
    -   Action - how (or where) the form data will be processed.
    -   Target - Where the result will open: ie same window (self) or in a new tab/window (blank)
    -   Name - each input needs a name value so the data can be labeled.
    -   Method - What HTTP method the form will use to send the form. GET or POST.
    -   Value - the initial value of the field.
    -   Placeholder - this is a “hint” that describes what should be entered in the field.
    -   Required - This field must have an input in order for the form to be submitted.
    -   Min and Max - give minimum or maximum values that can be imputed into the field.
-   The \<label> tag can be used to give a text label to an input field.
