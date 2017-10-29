# Codecadmey Notes: Unit 1 - HTML

##DAY ONE
### AN INTRODUCTION TO HTML

HTML = HyperText Markup Language

* **HTML Tag** - The element name, surrounded by an opening (<) and closing (>) angle bracket.
* **HTML element** (or simply, element) - a unit of content in an HTML document formed by HTML tags and the text or media it contains.
* **Opening tag** - the first HTML tag used to start an HTML element. The tag type is surrounded by opening and closing angle brackets.
* **Element content** - The information (text or other elements) contained between the opening and closing tags of an HTML element.
* **Closing tag** - the second HTML tag used to end an HTML element. Closing tags have a forward slash (/) inside of them, directly after the left angle bracket.

![HTML Element example][html-element-example]

##### REVIEW

1. HTML stands for HyperText Markup Language and is used to create the structure and content of a webpage.
1. Most HTML elements contain opening and closing tags with raw text or other HTML tags between them.
1. Single-closing tags cannot enclose raw text or other elements.
1. Comments are written in HTML using the following syntax: <!-- comment -->.
1. HTML elements can be nested inside other elements. The enclosed element is the child of the enclosing parent element.
1. Whitespace between HTML elements helps make code easier to read while not changing how elements appear in the browser.
1. Indentation also helps make code easier to read. It makes parent-child relationships visible.
1. The `<!DOCTYPE html>` declaration should always be the first line of code in your HTML files.
1. The `<html>` element will contain all of your HTML code.
1. Information about the web page, like the title, belongs within the `<head>` of the page.
1. You can add a title to your web page by using the `<title>` element, inside of the head.
1. A webpage's title appears in a browser's tab.
1. Code for visible HTML content is placed inside of the `<body>` element.

===

#DAY TWO
### HTML TAGS

* **Headings**: In HTML, there are six different headings, or heading elements. Headings can be used for a variety of purposes, like titling sections, articles, or other forms of content.

* **Paragraphs**: Paragraphs (`<p>`) simply contain a block of plain text.
* **Divs**: `<div>`s can contain any text or other HTML elements. They are primarily used to divide HTML documents into sections.
* **Spans**: `<span>`s contain short pieces of text or other HTML. They are primarily used to wrap small pieces of content that are on the same line as other content and do not break text into different sections.

* The `<em>` tag will generally render as italic emphasis.
* The `<strong>` will generally render as bold emphasis.

* **Line Breaks**: You may see line breaks written as `<br />` or `<br>`. Both are valid break tags. (Note: In HTML5, self-closing tags no longer need the '/' at the end of a tag.)

* **Unordered Lists**: In HTML, you can use an unordered list tag (`<ul>`) to create a list of items in no particular order. An unordered list outlines individual list items with a bullet point. The `<ul>` element cannot hold raw text and cannot automatically format raw text into an unordered list of items. Individual list items must be added to the unordered list using the `<li>` tag. The `<li>` or list item tag is used to describe an item in a list.
* **Ordered Lists**: Ordered lists are like unordered lists, except that each list item is numbered. You can create the ordered list with the `<ol>` tag and then add individual list items to the list using `<li>` tags.

* **Images**: The `<img>` tag has a required attribute called src. The src attribute must be set to the image's source, or the location of the image. In this case, the value of src must be the uniform resource locator (URL) of the image. A URL is the web address or local address where a file is stored. Note that the end of the `<img>` tag has a forward slash /. Self-closing tags may include or omit the final slash — both will render properly.
* **Videos**: Like the `<img>` tag, the `<video>` tag requires a src attribute with a link to the video source. Unlike the `<img>` tag however, the `<video>` element requires an opening and a closing tag. he video source (src=) is "myVideo.mp4." The source must link to a video file, not to a video on another site. After the src attribute, the width and height attributes are used to set the size of the video displayed in the browser. The controls attribute instructs the browser to include basic video controls: pause, play and skip. 

* **Links**: You can add links to a web page by adding an anchor element `<a>` and including the text of the link in between the opening and closing tags.
* **New Page**: For a link to open in a new window, the target attribute requires a value of _blank. The target attribute can be added directly to the opening tag of the anchor element, just like the href attribute.
* **Relative**: A relative path is a filename that shows the path to a local file (a file on the same website, such as ./index.html) versus an absolute path (a full url, like www.codecademy.com/learn/ruby which is stored in a different folder). The ./ in ./index.html tells the browser to look for the file in the current folder.
* **Same Page**: In order to link to a target on the same page, we must give the target an id. An id should be descriptive to make it easier to remember the purpose of a link. The target link is a string containing the # character and the target element's id.
* **Navication**: Linking to elements on the same page or to other pages on the same site is called navigation. HTML has a special tag called `<nav>` that is used to wrap these links in order to organize the content on your web page.

_**Semantic vs. Non-semantic Tags**: Some of the tags we have used, such as `<div>`, are called non-semantic tags. This means that they do not describe the content that is inside of them. However, many tags are used to describe the content that they surround, which helps us modify and style our content later. These are called semantic tags and `<nav>` is one of them!_

#### REVIEW

1. Headings and sub-headings, `<h1>` to `<h6>` tags, are used to enlarge text.
`<p>`, `<span>` and `<div>` tags specify text or blocks.
1. The `<em>` and `<strong>` tags are used to emphasize text.
1. Line breaks are created with the `<br>` tag.
1. Ordered lists (`<ol>`) are numbered and unordered lists (`<ul>`) are bulleted.
1. Images (`<img>`) and videos (`<video>`) can be added by linking to an existing source.
1. Anchor tags (`<a>`) are used to link to internal pages, external pages or content on the same page.
1. You can create sections on a webpage and jump to them using `<a>` tags and addings ids to the elements you wish to jump to.
1. The nav element contains links to internal pages or content.



<!-- Image Files -->

[html-element-example]: https://s3.amazonaws.com/codecademy-content/courses/web-101/htmlcss1-diagram__htmlanatomy.svg