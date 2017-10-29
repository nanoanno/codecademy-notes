# Codecadmey Notes: Unit 2 - CSS

## DAY ONE
### CSS SETUP

**CSS** means _Cascading Style Sheets_

Although CSS is a different language than HTML, it's possible to write CSS code directly within HTML code using inline styles.

To style an HTML element, you can add the `style` attribute directly to the opening tag. After you add the attribute, you can set it equal to the CSS style(s) you'd like applied to that element.

If you'd like to add more than one style with inline styles, simply keep adding to the `style` attribute. Make sure to end the styles with a semicolon (`;`).

### CSS SELECTORS
To style an HTML element, CSS first has to select it, using something called a CSS selector.

CSS always follows this two part process:
1. Select HTML elements.
1. Apply styles to the elements.

**Tag Names**: CSS can select HTML elements by using an element's tag name. A tag name is the word (or character) between HTML angle brackets. (For example, `p` for a paragraph tag.)
**Class Names**: To select an HTML element by its class using CSS, a period (`.`) must be prepended to the class's name. (For example, `class="test"` would be `.test`.)
**ID Names**: If an HTML element needs to be styled uniquely (no matter what classes are applied to the element), we can add an ID to the element. To add an ID to an element, the element needs an id attribute. Then, CSS can select HTML elements by their id attribute. To select an id element, CSS prepends the id name with a hashtag (`#`). (For example, `id="test-2"` ) would be `#test-2`.)

#### SPECIFICITY
Specificity is the order by which the browser decides which CSS styles will be displayed. A best practice in CSS is to style elements while using the lowest degree of specificity, so that if an element needs a new style, it is easy to override. IDs are the most specific selector in CSS, followed by classes, and finally, tags.

**Chaining Selectors**: When writing CSS rules, it's possible to require an HTML element to have two or more CSS selectors at the same time.
**Nested Elements:** In addition to chaining selectors to select elements, CSS also supports selecting elements that are nested within other HTML elements.
**Multiple Selectors**: In order to make CSS more concise, it's possible to add CSS styles to multiple CSS selectors all at once. This prevents writing repetitive code.
**Important**: There is one thing that is even more specific than IDs: !important. !important can be applied to specific attributes instead of full rules. It will override any style no matter how specific it is. As a result, it should almost never be used.

##### REVIEW 
* CSS can change the look of HTML elements. In order to do this, CSS must select HTML elements, then apply styles to them.
* CSS can select HTML elements by tag, class, or ID.
* Multiple CSS classes can be applied to one HTML element.
* Classes can be reusable, while IDs can only be used once.
* IDs are more specific than classes, and classes are more specific than tags. * That means IDs will override any styles from a class, and classes will override any styles from a tag selector.
* Multiple selectors can be chained together to select an element. This raises the specificity, but can be necessary.
* Nested elements can be selected by separating selectors with a space.
* The !important flag will override any style, however it should almost never be used, as it is extremely difficult to override.
* Multiple unrelated selectors can receive the same styles by separating the selector names with commas.

## DAY TWO
### CSS VISUAL RULES

CSS Structure: To style an HTML element using CSS, you need to write a CSS declaration inside the body of a CSS selector. CSS declarations consist of a property and a value.

* Property — the property you'd like to style of that element (i.e., size, color, etc.).
* Value — the value of the property (i.e., 18px for size, blue for color, etc.).

Note that a semicolon (;) is always used at the end of a declaration.

Finally, the entire code is known as a CSS rule. A CSS rule consists of the selector and all declarations inside of the selector.

#### FONT FAMILY
Font refers to the technical term typeface, or font family. To change the typeface of text on your web page, you can use the `font-family` property.

1. The font specified in a stylesheet must be installed on a user's computer in order for that font to display when a user visits the web page.
The default typeface for all HTML elements is Times New Roman. You may be familiar with this typeface if you have ever used a formatted word processor.
1. If no font-family attribute is defined, the page will appear in Times New Roman.
1. It's a good practice to limit the number of typefaces used on a web page to 2 or 3. This helps the page load faster in some cases and is usually a good design decision.
1. When the name of a typeface consists of more than one word, it's a best practice to enclose the typeface's name in quotes, like so:

#### FONT SIZE
To change the size of text on your web page, you can use the `font-size` property. `px` means pixels and is a way to measure font size.

#### FONT WEIGHT
In CSS, the `font-weight` property controls how bold or thin text appears.

#### TEXT ALGIN
No matter how much styling is applied to text (typeface, size, weight, etc.), text always appears on the left side of the browser. To align text we can use the `text-align` property. The `text-align` property will align text to the element that holds it, otherwise known as its parent.

The text-align property can be set to one of the following three values:

1. left — aligns text to the left hand side of its parent element, which in this case is the browser.
1. center — centers text inside of its parent element.
1. right — aligns text to the right hand side of its parent element.

#### COLOR
Before discussing the specifics of color, it's important to make two distinctions about color. Color can affect the following design aspects: 

* Foreground color
* Background color
Foreground color is the color that an element appears in. For example, when a heading is styled to appear green, the foreground color of the heading has been styled.

Conversely, when a heading is styled so that its background appears yellow, the background color of the heading has been styled.

In CSS, these two design aspects can be styled with the following two properties:

* `color`: this property styles an element's foreground color
* `background-color`: this property styles an element's background color

#### OPACITY
Opacity is the measure of how transparent an element is. It's measured from 0 to 1, with 1 representing 100%, or fully visible and opaque, and 0 representing 0%, or fully invisible.

#### BACKGROUND IMAGE
CSS has the ability to change the background of an element. One option is to make the background of an element an image. This is done through the CSS property `background-image`.

1. The `background-image` property will set the element's background to display an image.
1. The value provided to background-image is a `url`. The `url` should be a `url` to an image. The `url` can be a file within your project, or it can be a link to an external site. To link to an image inside an existing project, you must provide a relative file path. If there was an image folder in the project, with an image named mountains.jpg, the relative file path would look like: `background-image: url("images/mountains.jpg");`

##### REVIEW
* CSS declarations are structured into property and value pairs.
* The `font-family` property defines the typeface of an element.
* `font-size` controls the size of text displayed.
* `font-weight` defines how thin or thick text is displayed.
* The `text-align` property places text in the left, right, or center of its parent container.
* Text can have two different color attributes: `color` and `background-color`. `color` defines the color of the text, while `background-color` defines the color behind the text.
* CSS can make an element transparent with the `opacity` property.
* CSS can also set the background of an element to an image with the `background-image` property.





