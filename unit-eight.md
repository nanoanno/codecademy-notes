# Codecadmey Notes: Unit 8 - Capstone Project - Colmar Academy

## DAY TWO
### FONT AWESOME

#### LINK FONT AWESOME

The Font Awesome library is linked to an HTML document using the `<link>` tag. The library can be linked from a CDN or saved and linked to a local file.

Boostrap CDN:
```html
<head>
  <link rel="stylesheet" type="text/css" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.css">
</head>
```

Font Awesome icons are saved as CSS classes. They are placed into an HTML document by adding an `<i>` tag with two classes: `fa` and `fa-icon-name`, where `fa-icon-name` refers to the icon-specific class name.

`<i class="fa fa-save"></i>`

In the example above, the `<i>` tag's class is `fa fa-save`. The `fa` class is required for all Font Awesome icon elements. It provides standard size and display values for the icon, without which, the icon would not appear properly. The `fa-save` class references the floppy disc image. If Font Awesome is correctly loaded in the head of the document, the floppy disc icon will appear on the HTML page.

Use the Font Awesome cheat sheet to find Font Awesome icons and their matching classes: http://fontawesome.io/cheatsheet/

Font Awesome supports additional classes for icon sizing.

Icon size can be increased by 33% with `fa-lg`, two times with `fa-2x`, three times with `fa-3x`, four times with `fa-4x`, or five times with `fa-5x`.

## DAY FOUR
### MANAGING ASSETS AND ICONS

Types of Image Files: 

1. JPEG - a highly compressible file type that is preferred for images with significant detail
1. PNG - a file type that is lossless (meaning that full quality is maintained) - generally preferred for images with less detail such as logos
1. SVG - useful for high resolution screens, scalable vector graphics (SVG) will change size (scale) for various screen sizes; SVGs also contain roughly 50% less data than their JPEG or PNG equivalents allowing web pages to load more quickly; they are becoming widely used for simple images such as icons and logos

A good practice is to select JPEG for more detailed images and PNG for images with more empty space. If you select JPEG, you'll also have to select quality. The web standard for JPEG files is 85%.

Favicon generator: https://www.favicon-generator.org/

To add the favicon to your web page, add the file to your project directory and add this code to the `<head>` of your HTML document. `<link rel="icon" href="./<favicon-name>.ico" type="image/x-icon">`

Pixlr: https://pixlr.com/editor/
Online-Convert: https://image.online-convert.com/convert-to-svg

## DAYS FIVE-SEVEN
### ACCESSIBILITY AND ARIA

The Web Accessibility Initiative (https://en.wikipedia.org/wiki/Web_Accessibility_Initiative) (led by W3C) developed standards for making information on the Internet accessible to all.

These standards fall under a group of guidelines called ARIA (https://en.wikipedia.org/wiki/WAI-ARIA), or Accessible Rich Internet Applications. These guidelines are easily implemented and make web pages accessible to a broader audience.

#### SEMANTIC HTML TAGS
The quickest way of improving accessibility for screen readers is to use the appropriate tags for a given task.

#### ARIA
To help add context to web page information, ARIA provides an HTML attribute called role. The value of an element's role changes how a screen reader communicates the element.

```html
<div id="code-editor" role="complementary">
  ...
</div>
```

The `role="complementary"` attribute and value can help a screen reader user understand that the information in the code editor is complementary (or supporting) to the information you are reading right now. It helps users of screen readers identify the relationship between the two sections of the page.

This link (https://www.w3.org/TR/html-aria/#allowed-aria-roles-states-and-properties) has a list of acceptable ARIA roles, where you can read more about the complementary role and other roles as well.

We can instruct screen readers to skip reading unnecessary elements by setting the `role` attribute to `presentation`.

The `presentation` role skips over elements and their _necessary_ children. The `<ol>` and `<ul>` elements require `<li>` children. Therefore, adding `role="presentation"` to an ol tag will cause the screen reader to skip directly to the text between the `<li>` tags (it will not read the names of the `<li>` elements).

Additional reading on presentation: https://w3c.github.io/using-aria/#presentation

ARIA properties are attributes that you can add to HTML elements. These attributes provide additional information about elements that might not be obvious to users of screen readers. Let's explore a property called `aria-label`.

```html
<img src="#" alt="A painting of the Shenandoah Valley"/>
<p>Armand Cabrera, 2010</p>
```

In the example above, a person looking at the web page would likely see "Armand Cabrera" below the image and use visual clues to infer that he is the artist. However, for someone using a screen reader it might not be clear what the paragraph below the image means. The property `aria-label` gives the screen reader additional information to read out loud to the user.

```html
<img src="#" alt="A painting of the Shenandoah Valley"/>
<p aria-label="Artist">Armand Cabrera, 2010</p>
```

In the improved HTML above, a user of a screen reader will know how this paragraph relates to the image above it.

Other ARIA properties are useful in more complex websites using HTML forms, JavaScript, and other advanced tools.

For a complete list of ARIA properties, click this link: https://www.w3.org/TR/wai-aria/states_and_properties

#### ALT ATTRIBUTE
Some HTML elements have a built-in attribute called alt that works like `aria-label` but has additional functionality.

The `alt` attribute is used to describe an image (or several other elements). A screen reader will read the value of the `alt` attribute out loud. However, if the element cannot be visually seen — whether it is because the user is visually impaired, an incorrect source is referenced, or the page is being accessed over a slow connection — the `alt` attribute will be displayed in its place.

On the other hand, the value of `aria-label` will never be displayed on the screen and is a better choice for elements that do not support the `alt` attribute.

When using the alt attribute, you should adhere to these conventions:

1. In general, the value of `alt` should concisely describe the image.
1. For images that are also `<a>` elements, the alt attribute should describe the source that the link targets.
1. If an image conveys no information (such as a decorative border), the `alt` attribute should be empty, but should never be omitted.
1. If an image is described by text near the image, do not duplicate the description in the `alt` attribute. Use an empty `alt` attribute instead.
1. The value of an `alt` attribute should be no more than 150 characters.

##### Review
Using ARIA roles and properties, `alt` attributes, and semantic elements in your HTML is a simple way to make your website accessible to visually-impaired Internet users.

1. Using semantic HTML elements whenever possible (such as `<header>` instead of `<div id="header">`) will allow screen reader users to navigate your website more efficiently.
1. The `role` attribute is used to communicate information about the role of specific elements.
1. `role="presentation"` allows a screen reader to skip markup elements that don't directly contain useful information.
1. `aria-label` and other ARIA properties can be used to help users perceive information that is communicated visually but not through text.
1. The `alt` attribute should be added to every image element (and all other elements that support it) instead of aria-label. When used, its value should be a useful description of the image.







