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





