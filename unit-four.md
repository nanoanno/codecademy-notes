# Codecadmey Notes: Unit 4 - Display and Positioning

##DAY ONE
###Lesson: The Box Model

The box model comprises the set of properties which define parts of an element that take up space on a web page. The model includes the content area's size (width and height) and the element's padding, border, and margin. The properties include:

1. Width and height — specifies the width and height of the content area.
1. Padding — specifies the amount of space between the content area and the border.
1. Border — specifies the thickness and style of the border surrounding the content area and padding.
1. Margin — specifies the amount of space between the border and the outside edge of the element.

The image below is a visual representation of the box model.

![box-model][box-model]

####Height and Width
An element's content has two dimensions: a height and a width. By default, the dimension of an HTML box are set to hold the raw contents of the box.

The CSS `height` and `width` properties can be used to modify these default dimensions.

####Borders
A _border_ is a line that surrounds an element, like a frame around a painting. Borders can be set with a specific `width`, `style`, and `color`.

* `width` — The thickness of the border. A border's thickness can be set in pixels or with one of the following keywords: `thin`, `medium`, or `thick`.
* `style` — The design of the border. Web browsers can render any of 10 different styles. Some of these styles include: `none`, `dotted`, and `solid`.
* `color` The color of the border. Web browsers can render colors using a few different formats, including 140 built-in color keywords.

####Padding
The space between the contents of a box and the borders of a box is known as padding. Padding is like the space between a picture and the frame surrounding it. In CSS, you can modify this space with the `padding` property.

If you want to be more specific about the amount of padding on each side of a box's content, you can use the following properties:

1. `padding-top`
1. `padding-right`
1. `padding-bottom`
1. `padding-left`

Another implementation of the `padding` property lets you specify exactly how much padding there should be on each side of the content in a single declaration.

####Margins

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

####Overflow
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


#####Review
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







[box-model]: https://s3.amazonaws.com/codecademy-content/courses/freelance-1/unit-4/diagram-boxmodel.svg
[margin-collapse]: https://s3.amazonaws.com/codecademy-content/courses/freelance-1/unit-4/diagram-verticalmargins.svg