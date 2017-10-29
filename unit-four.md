# Codecadmey Notes: Unit 4 - Display and Positioning

## DAY ONE
### LESSON: THE BOX MODEL

The box model comprises the set of properties which define parts of an element that take up space on a web page. The model includes the content area's size (width and height) and the element's padding, border, and margin. The properties include:

1. Width and height — specifies the width and height of the content area.
1. Padding — specifies the amount of space between the content area and the border.
1. Border — specifies the thickness and style of the border surrounding the content area and padding.
1. Margin — specifies the amount of space between the border and the outside edge of the element.

The image below is a visual representation of the box model.

![box-model][box-model]

#### Height and Width
An element's content has two dimensions: a height and a width. By default, the dimension of an HTML box are set to hold the raw contents of the box.

The CSS `height` and `width` properties can be used to modify these default dimensions.

#### Borders
A _border_ is a line that surrounds an element, like a frame around a painting. Borders can be set with a specific `width`, `style`, and `color`.

* `width` — The thickness of the border. A border's thickness can be set in pixels or with one of the following keywords: `thin`, `medium`, or `thick`.
* `style` — The design of the border. Web browsers can render any of 10 different styles. Some of these styles include: `none`, `dotted`, and `solid`.
* `color` The color of the border. Web browsers can render colors using a few different formats, including 140 built-in color keywords.

#### Padding
The space between the contents of a box and the borders of a box is known as padding. Padding is like the space between a picture and the frame surrounding it. In CSS, you can modify this space with the `padding` property.

If you want to be more specific about the amount of padding on each side of a box's content, you can use the following properties:

1. `padding-top`
1. `padding-right`
1. `padding-bottom`
1. `padding-left`

Another implementation of the `padding` property lets you specify exactly how much padding there should be on each side of the content in a single declaration.

#### Margins

Margin refers to the space directly outside of the box. The `margin` property is used to specify the size of this space.

If you want to be even more specific about the amount of margin on each side of a box, you can use the following properties:

1. `margin-top`
1. `margin-right`
1. `margin-bottom`
1. `margin-left`

Just like the padding shortcut, when you're certain that the top and bottom values for margin will equal each other, and that the left and right values for margin will also equal each other, you can use the shortcut. 

**Auto:**
The `margin` property also lets you center content. However, you must follow a few syntax requirements. 

In this example , `margin: 0 auto;` will center the divs in their containing elements. The `0` sets the top and bottom margins to `0` pixels. The `auto` value instructs the browser to adjust the left and right margins until the element is centered within its containing element.

Note: In order to center an element, a width must be set for that element. It's not possible to center an element that takes up the full width of the page.

**Margin Collapse:**
As you have seen, padding is space added inside an element's border, while margin is space added outside an element's border. One additional difference is that top and bottom margins, also called vertical margins, collapse, while top and bottom padding does not.

Horizontal margins (left and right), like padding, are always displayed and added together. 

It may be helpful to think of collapsing vertical margins as a short person trying to push a taller person. The tall person has longer arms and can easily push the short person, while the person with short arms cannot reach the person with long arms.

Example: 
Study the graphic display to the right. Elements A and B have 20 pixels of horizontal margin, the sum of each element's margin. Elements A and C have 30 pixels of vertical margin — the top margin of element C.

![margin-collapse][margin-collapse]

#### Overflow
All of the components of the box model comprise an element’s size. For example, an image that has the following dimensions is 364 pixels wide and 244 pixels tall.

* 300 pixels wide
* 200 pixels tall
* 10 pixels padding on the left and right
* 10 pixels padding on the top and bottom
* 2 pixels border on the left and right
* 2 pixels border on the top and bottom
* 20 pixels margin on the left and right
* 10 pixels margin on the top and bottom

The total dimensions (364px by 244px) are calculated by adding all of the vertical dimensions together and all of the horizontal dimensions together. Sometimes, these components result in an element that is larger than the parent's containing area.

The `overflow` property controls what happens to content that spills, or overflows, outside its box. It can be set to one of the following values:

* `hidden` - when set to this value, any content that overflows will be hidden from view.
* `scroll` - when set to this value, a scrollbar will be added to the element's box so that the rest of the content can be viewed by scrolling.
* `visible` - when set to this value, the overflow content will be displayed outside of the containing element. Note, this is the default value.


##### Review
In th1. is lesson, we covered the four properties of the box model: height and width, padding, borders, and margins. Understanding the box model is an important step towards learning more advanced HTML and CSS topics. Let's take a minute to review what you learned.

1. The box model comprises a set of properties used to create space around and between HTML elements.
1. The height and width of a content area can be set in pixels or percentage.
1. Borders surround the content area and padding of an element. The color, style, and thickness of a border can be set with CSS properties.
1. Padding is the space between the content area and the border. It can be set in pixels or percent.
1. Margin is the amount of spacing outside of an element's border.
1. Horizontal margins add, so the total space between the borders of adjacent elements is equal to the sum of the right margin of one element and the left margin of the adjacent element.
1. Vertical margins collapse, so the space between vertically adjacent elements is equal to the larger margin.
1. `margin: 0 auto` horizontally centers an element inside of its parent content area, if it has a width.
1. The `overflow` property can be set to `display`, `hide`, or `scroll`, and dictates how HTML will render content that overflows its parent's content area.

## DAY TWO-THREE
### LESSON: CSS DISPLAY

#### Inline Display
Every HTML element has a default `display` value that dictates if it can share horizontal space with other elements. Some elements fill the entire browser from left to right regardless of the size of their content. Other elements only take up as much horizontal space as their content requires and can be directly next to other elements.

In this lesson, we’ll cover three values for the `display` property: `inline`, `block`, and `inline-block`.

(The default display for some tags, such as `<em>`, `<strong>`, and `<a>`, is called inline. Inline elements have a box that wraps tightly around their content, only taking up the amount of space necessary to display their content and not requiring a new line after each element. The height and width of these elements cannot be specified in the CSS document.)

The CSS `display` property provides the ability to make any element an inline element. 

#### Block Display
Some elements are not displayed in the same line as the content around them. These are called __block-level__ elements. These elements fill the entire width of the page and, unless specified, are the height necessary to accommodate the content inside.

Elements that are block-level by default include all levels of heading elements (`<h1>` through `<h6>`), `<p>`, `<div>` and `<footer>`.

Complete list of block elements: https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements

#### Inline-Block Display
The third value for the `display` property is `inline-block`. Inline-block display combines features of both inline and block elements. Inline-block elements can appear next to each other and we can specify their dimensions using the `width` and `height` properties. Images are the best example of default inline-block elements.

#### Positioning
The `position` property specifies where an element is placed in relation to other elements and whether the element moves when the user scrolls. Just as all elements have a default `display` value, they also have a default `position` value. We can change the default position of an element by setting its position property. The position property can take one of four values:

1. `static` — an element will be positioned where it naturally occurs in the flow of the document from left to right, top to bottom (the default value).
1. `absolute` — an element will be positioned exactly where it is specified in relation to the nearest non-statically positioned element; it is removed from the flow of the web page.
1. `relative` — an element will be positioned in relation to where it would have occurred in the flow of the document; it is NOT removed from the flow and space is reserved for it.
1. `fixed` — an element will be positioned in the same place in the viewport of the browser (the part of the browser that contains the website being viewed) at all times, even if the user scrolls; it is removed from the flow of the web page.

#### Absolute
The first consideration is that when an element's positioning is set to absolute, the element is removed from the flow of the document and no space is reserved for it. The element is essentially floating on top of the rest of the content. This means that all elements that come after it will shift up and/or to the left, depending on the `display` values for those elements.

The next thing to keep in mind is that when an element’s position is changed to absolute, the element will move to the top left of the nearest container element that is not statically positioned. If no elements on the page have position declarations, the element will move to the top left of the view and move as the user scrolls. If the parent container of an element (such as a `div` that contains an image) is positioned, the absolutely positioned element (the image) will be positioned relative to the containing element (the `div`).

There are 4 values for offsetting position:

1. `top` — specifies how far from the top of the non-static parent container the element should be.
1. `left` — specifies how far from the left of the non-static parent container the element should be.
1. `right` — specifies how far from the right of the non-static parent container the element should be.
1. `bottom` — specifies how far from the bottom of the non-static parent container the element should be.

#### Fixed
Fixed positioning causes an element to remain visible to the user at all times; even when scrolling, a fixed element will not move. 

#### Relative
Unlike `absolute` and `fixed` positioning, `relative` positioning does not remove an element from the flow of an HTML document.

#### Z-index
The `z-index` property controls how far "back" or how far "forward" a non-static element should appear on the web page. The `z-index` property accepts integer values. These values instruct the browser in which order to display the elements on the web page.

The default value of `z-index` is `auto`. In practice, the browser will search for the `z-index` of the parent elements until it finds one. If none of the parent elements have a `z-index` declared, the `z-index` of the element will default to `0`. Therefore, it is not necessary to set the `z-index` of `.description` to `0`, as `.description` does not have a parent element with a `z-index` other than `0`. Negative `z-index` values are not accepted. Setting the `z-index` of `.navigation` to a number greater than `0` is sufficient to prevent overlapping content. `z-index` values are somewhat arbitrary — they don't need to start at `1`. Any element that you wish to display in front of another item simply needs a `z-index` greater than the element beneath it.

##### Review
Review

1. The default positioning of elements is based on the __flow__ of the HTML file.
1. Inline elements appear next to each other on the same line.
1. You can position elements to be displayed on their own line using block display.
1. Inline-block elements are on the same line as each other and their size can be set.
1. The default positioning for any element is `static` which means it will appear exactly as it does in the flow of the HTML document.
1. Elements with `absolute` positioning are removed from the flow of the document and positioned in relation to the parent element. This positioning will override display properties. An element with absolute positioning will scroll.
1. Elements with `fixed` positioning will not scroll as the page scrolls. This removes the element from the flow of the document.
1. Elements with `relative` positioning specify the element's distance from where it would have been positioned in the flow of the HTML document.
1. Non-static elements can be displayed in front or behind another element using the `z-index` property.

## DAYS FOUR-FIVE
### FLEXBOX

Display options:
`display: flex;`
`display: inline-flex;`


`justify-content`

1. `flex-start` — all items will be positioned in order starting, from the left of the parent container, with no extra space between or before them.
1. `flex-end` — all items will be positioned in order, with the last item starting on the right side of the parent container, with no extra space between or after them.
1. `center` — all items will be positioned in order, in the center of the parent container with no extra space before, between, or after them.
1. `space-around` — items will be positioned with equal space before and after each item, resulting in double the space between elements.
1. `space-between` — items will be positioned with equal space between them, but no extra space before the first or after the last elements.


`align-items`

1. `flex-start` — all elements will be positioned at the top of the parent container.
1. `flex-end` — all elements will be positioned at the bottom of the parent container.
1. `center` — the center of all elements will be positioned halfway between the top and bottom of the parent container.
1. `baseline` — the bottom of the content of all items will be aligned with each other.
1. `stretch` — if possible, the items will stretch from top to bottom of the container (this is the default value; elements with a specified height will not stretch; elements with a minimum height or no height specified will stretch).


`flex-grow` (defulat is `0`)
`flex-shrink` (defulat is `1`)


`flex-basis` allows us to specify the width of an item before it stretches or shrinks.
The `flex` property allows you to declare `flex-grow`, `flex-shrink`, and `flex-basis` all in one line.


`flex-wrap`

1. `wrap` — child elements of a flex container will move down to the next line starting from the final item and working towards the first.
1. `nowrap` — prevents items from wrapping; this is the default value and is only necessary to override a wrap value set by a different CSS rule.
1. `wrap-reverse` — the wrapped element is displayed on top of the other elements in the flex container starting from the last and working toward the first (a mirror image of the wrap value).
Note: The `flex-wrap` property is declared on flex containers.


`align-content`

1. `flex-start` — all rows of elements will be positioned at the top of the parent container with no extra space between.
1. `flex-end` — all rows of elements will be positioned at the bottom of the parent container with no extra space between.
1. `center` — all rows of elements will be positioned at the center of the parent element with no extra space between.
1. `space-between` — all rows of elements will be spaced evenly from the top to the bottom of the container with no space above the first or below the last.
1. `space-around` — all rows of elements will be spaced evenly from the top to the bottom of the container with the same amount of space at the top and bottom and between each element.
1. `stretch` — if a minimum height or no height is specified, the rows of elements will stretch to fill the parent container from top to bottom (default value).

The major axis is used to position flex items with the following properties:
`justify-content`
`flex-wrap`
`flex-grow`
`flex-shrink`

The cross axis is used to position flex items with the following properties:
`align-items`
`align-content`

The major axis and cross axis are interchangeable. We can switch them using the `flex-direction` property. If we add the `flex-direction` property and give it a value of `column`, the flex items will be ordered vertically, not horizontally.

`flex-direction`

1. `row` — elements will be positioned from left to right across the parent element starting from the top left corner (default).
1. `row-reverse` — elements will be positioned from right to left across the parent element starting from the top right corner.
1. `column` — elements will be positioned from top to bottom of the parent element starting from the top left corner.
1. `column-reverse` — elements will be positioned from the bottom to the top of the parent element starting from the bottom left corner.

Like the `flex` property, the `flex-flow` property is used to declare both the `flex-wrap` and `flex-direction` properties in one line.

##### REVIEW

1. `display: flex` changes an element to a block-level container with flex items inside of it.
1. `display: inline-flex` allows multiple flex containers to appear inline with each other.
1. `justify-content` is used to space items along the major axis.
1. `align-items` is used to space items along the cross axis.
1. `flex-grow` is used to specify how much space (and in what proportions) flex items absorb along the major axis.
1. `flex-shrink` is used to specify how much flex items shrink and in what proportions along the major axis.
1. `flex-basis` is used to specify the initial size of an element styled with  `flex-grow` and/or `flex-shrink`.
1. `flex` is used to specify `flex-grow`, `flex-shrink`, and `flex-basis` in one declaration.
1. `flex-wrap` specifies that elements should shift along the cross axis if the flex container is not large enough.
1. `align-content` is used to space rows along the cross axis.
1. `flex-direction` is used to specify the major and cross axes.
1. `flex-flow` is used to specify `flex-wrap` and `flex-direction` in one declaration.
1. Flex containers can be nested inside of each other by declaring `display: flex` or `display: inline-flex` for children of flex containers.1. 






[box-model]: https://s3.amazonaws.com/codecademy-content/courses/freelance-1/unit-4/diagram-boxmodel.svg
[margin-collapse]: https://s3.amazonaws.com/codecademy-content/courses/freelance-1/unit-4/diagram-verticalmargins.svg