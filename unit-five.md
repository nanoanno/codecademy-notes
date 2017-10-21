# Codecadmey Notes: Unit 5 - Responsive Design

##DAY ONE
###LESSON: 

Responsive design refers to the ability of a website to resize and reorganize its content based on:

1. The size of other content on the website.
1. The size of the screen the website is being viewed on.

####Em

The em represents the size of the base font being used. For example, if the base font of a browser is 16 pixels (which is normally the default size of text in a browser), then 1 em is equal to 16 pixels. 2 ems would equal 32 pixels, and so on.

####Rem

Rem stands for root em. It acts similar to em, but instead of checking parent elements to size font, it checks the root element. The root element is the `<html>` tag.

Example of code commonly uesd for images:

.container {
  width: 50%;
  height: 200px;
  overflow: hidden;
}

.container img {
  max-width: 100%;
  height: auto;
  display: block;
}


background image scaling: 

body {
  background-image: url('#');
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

* Content on a website can be sized relative to other elements on the page using _relative measurements_.
* The unit of `em` sizes font relative to the font size of a parent element.
* The unit of `rem` sizes font relative to the font size of a root element. That root element is the <html> element.
* Percentages are commonly used to size box-model features, like the width, height, borders, padding, or margin of an element.
* When percentages are used to size width and height, child elements will be sized relative to the dimensions of their parent (remember that parent dimensions must first be set).
* Percentages can be used to set padding and margin. Horizontal and vertical padding and margin are set relative to the width of a parent element.
* The minimum and maximum width of elements can be set using `min-width` and `max-width`.
* The minimum and maximum height of elements can be set using `min-height` and `max-height`.
* When the height of an image or video is set, then its width can be set to `auto` so that the media scales proportionally. Reversing these two properties and values will also achieve the same result.
* A background image of an HTML element will scale proportionally when its `background-size` property is set to `cover`.

##DAY TWO
###MEDIA QUERIES

Breakdown of Media Query components: 

1. `@media` — This keyword begins a media query rule and instructs the CSS compiler on how to parse the rest of the rule.
1. `only screen` — Indicates what types of devices should use this rule. In early attempts to target different devices, CSS incorporated different media types (screen, print, handheld). The rationale was that by knowing the media type, the proper CSS rules could be applied. However, “handheld” and “screen” devices began to occupy a much wider range of sizes and having only one CSS rule per media device was not sufficient. `screen` is the media type always used for displaying content, no matter the type of device. The only keyword is added to indicate that this rule `only` applies to one media type (`screen`).
1. `and (max-width : 480px)` — This part of the rule is called a _media feature_, and instructs the CSS compiler to apply the CSS styles to devices with a width of 480 pixels or smaller. Media features are the conditions that must be met in order to render the CSS within a media query.
1. CSS rules are nested inside of the media query's curly braces. The rules will be applied when the media query is met. In the example above, the text in the `body` element is set to a `font-size` of `12px` when the user's screen is less than 480px.

####Range

```css
@media only screen and (min-width: 320px) and (max-width: 480px) {
    /* ruleset for 320px - 480px */
}
```

```css
@media only screen and (min-width: 320px) { 
    /* ruleset for 320px - 479px */
}


@media only screen and (min-width: 480px) { 
    /* ruleset for > 480px */
}
```

####Dots Per Inch (DPI)

To target by resolution, we can use the `min-resolution` and `max-resolution` media features. 

```css
@media only screen and (min-resolution: 300dpi) {
    /* CSS for high resolution screens */
}
```

####And Operator
