# Codecadmey Notes: Unit 7 - Design and UI Feedback

## DAY ONE
### CSS COLOR

#### INTRODUCTION TO COLOR
Colors in CSS can be described in three different ways:

* _Named colors_ — English words that describe colors, also called _keyword_ colors
* _RGB_ — numeric values that describe a mix of red, green, and blue
* _HSL_ — numeric values that describe a mix of hue, saturation, and lightness

#### HEXADECIMAL
A hex color begins with a hash character (`#`) which is followed by three or six characters. The characters represent values for red, blue and green.

The hexadecimal number system has 16 digits (0-15) instead of 10 (0-9) like you are used to. To represent 10-15, we use A-F. Here (https://developer.mozilla.org/en-US/docs/Web/CSS/color_value) is a list of many different colors and their hex values.

#### RGB COLORS
There is another syntax for representing RGB values that uses decimal numbers. It looks like this: `css color: rgb(23, 45, 23);` Here, each of the three values represents a color component, and each can have a decimal number value from 0 to 255. The first number represents the amount of red, the second is green, and the third is blue. These colors are exactly the same as hex, but with a different syntax and a different number system.

#### HEX AND RGB
In both hex and decimal, we have three values, one for each color. Each can be one of 256 values. Specifically, `256 * 256 * 256 = 16,777,216`. That is the amount of colors we can now represent. Compare that to the 147 named CSS colors!

#### HUE, SATURATION, AND LIGHTNESS
The syntax for HSL is similar to the decimal form of RGB, though it differs in important ways. The first number represents the degree of the hue, and can be between 0 and 360. The second and third numbers are percentages representing saturation and lightness respectively. Here is an example: `color: hsl(120, 60%, 70%);`

_Hue_ is the first number. It refers to an angle on a color wheel. Red is 0 degrees, Green is 120 degrees, Blue is 240 degrees, and then back to Red at 360. You can see an example of this color wheel here (http://dba.med.sc.edu/price/irf/Adobe_tg/models/images/hsl_top.JPG).

_Saturation_ refers to the intensity or purity of the color. If you imagine a line segment drawn from the center of the color wheel to the perimeter, the saturation is a point on that line segment. If you spin that line segment to different angles, you'll see how that saturation looks for different hues. The saturation increases towards 100% as the point gets closer to the edge (the color becomes more rich). The saturation decreases towards 0% as the point gets closer to the center (the color becomes more gray).

_Lightness_ refers to how light or dark the color is. Halfway, or 50%, is normal lightness. Imagine a sliding dimmer on a light switch that starts halfway. Sliding the dimmer up towards 100% makes the color lighter, closer to white. Sliding the dimmer down towards 0% makes the color darker, closer to black.

#### OPACITY AND ALPHA
To use opacity in the HSL color scheme, use `hsla` instead of `hsl`, and four values instead of three. For example: `color: hsla(34, 100%, 50%, 0.1);`

The fourth value (which we have not seen before) is the _alpha_. This last value is sometimes called the opacity. Alpha is a decimal number from zero to one. If alpha is zero, the color will be completely transparent. If alpha is one, the color will be opaque.

The RGB color scheme has a similar syntax for opacity, rgba. Again, the first three values work the same as rgb and the last value is the alpha. Here's an example: `color: rgba(234, 45, 98, 0.33);`

Alpha can only be used with HSL and RGB colors. There is, however, a named color keyword for zero opacity, `transparent`. It's equivalent to r`gba(0, 0, 0, 0)`. It's used like any other color keyword: `color: transparent;`

##### REVIEW
There are four ways to represent color in CSS:

* Named colors — there are 147 named colors, which you can review here (https://developer.mozilla.org/en-US/docs/Web/CSS/color_value).
* Hexadecimal or hex colors
    * Hexadecimal is a number system with has sixteen digits, 0 to 9 followed by "A" to "F".
    * Hex values always begin with `#` and specify values of red, blue and green using hexademical numbers such as `#23F41A`.
* RGB
    * RGB colors use the `rgb()` syntax with one value for red, one value for blue and one value for green.
    * RGB values range from 0 to 255 and look like this: `rgb(7, 210, 50)`.
* HSL
    * HSL stands for hue (the color itself), saturation (the intensity of the color), and lightness (how light or dark a color is).
    * Hue ranges from 0 to 360 and saturation and lightness are both represented as percentages like this: `hsl(200, 20%, 50%)`.  
* You can add opacity to color in RGB and HSL by adding a fourth value, `a`, which is represented as a percentage.

### DESIGN - COLOR

#### THINKING ABOUT COLOR

Questions to ask yourself: 

* What color is the text and its background?
* How many different colors can you spot?
* Does the set of colors feel like they go together?
* If there are buttons, what color are they?
* If there are images, how do the colors in the image fit into the rest of the page?

* Where does color fit into the author's CSS?
* What color scheme (RGB or HSL) do the authors use?
* Does anything about the use of color surprise you?

Inspiration: 

* Dribble: https://dribbble.com/
* Site Inspire: https://www.siteinspire.com/
* Awwwards: https://www.awwwards.com/

#### DECIDING ON COLORS

Tools: 

* Paletton: http://paletton.com/
* Adobe Color CC: https://color.adobe.com/

Rules: 

* Monochromatic — Variations on a single hue
* Analogous — Hues equidistant from each other (usually adjacent) on the color wheel and variations on these
* Complementary — Hues opposite each other on the color wheel and variations on these

#### ACCESSIBLE COLORS

* Color Blindness: http://www.colourblindawareness.org/colour-blindness/
* Color Lab: http://colorlab.wickline.org/colorblind/colorlab/

## DAY TWO
### CSS - TYPOGRAPHY

#### FONT WEIGHT
In CSS, we can style bold text with the font-weight property: `font-weight: bold;`

If we want to ensure that text is not bold, we can set the `font-weight` to `normal`.

The `font-weight` property can also be assigned a number value to style text on a numeric scale ranging from 100 to 900. Valid values are multiples of 100 within this range.

When using numeric weights, there are a number of default font weights that we can use:

* `400` is the default `font-weight` of most text.
* `700` signifies a bold `font-weight`.
* `300` signifies a light `font-weight`.

#### FONT STYLE
You can also italicize text with the `font-style` property. The `italic` value causes text to appear in italics. The `font-style` property also has a `normal` value which is the default.

#### LINE HEIGHT
We can use the line-height property to set how tall we want the line containing our text to be, regardless of the height of the text. Line heights can take one of several values:

* A unitless number, such as `1.2`. This number is an absolute value that will compute the line height as a ratio of the font size.
* A number specified by unit, such as `12px`. This number can be any valid CSS unit, such as pixels, percents, ems, or rems.

#### SERIF AND SANS SERIF
Over time, typographers have refined their craft and have developed many different typefaces, allowing them to classify typefaces, in most cases, as one of the following: _serif_ fonts and _sans-serif_ fonts.

1. _Serif_ — fonts that have extra details on the ends of each letter. Examples include fonts like Times New Roman or Georgia, among others.
1. _Sans-Serif_ — fonts that do not have extra details on the ends of each letter. Instead, letters have straight, flat edges, like Arial or Helvetica.

#### FALLBACK FONTS
Most computers have a small set of typefaces pre-installed. This small set includes serif fonts like Times New Roman and sans-serif fonts like Arial. These pre-installed fonts serve as fallback fonts if the stylesheet specifies a font which is not installed on a user's computer.

To use fallback fonts, the following syntax is required:

``` css
h1 {
  font-family: "Garamond", "Times", serif;
}
```

The CSS rule above says:

1. Use the Garamond font for all `<h1>` elements on the web page.
1. If Garamond is not available, use the Times font.
1. If Garamond and Times are not available, use any serif font pre-installed on the user's computer.

The fonts specified after Garamond are the fallback fonts (`Times`, `serif`). Fallback fonts help ensure a consistent experience for the diverse audience of users that visit a site.

#### LINKING FONTS
With the number of fonts available with modern typography, it is unrealistic to expect users to have all fonts installed on their computers. New fonts are often centralized in directories made available for public use. We refer to these fonts as non-user fonts.

Google Fonts (https://fonts.google.com/) is one such directory of thousands of open-source fonts, available for free use. Google Fonts gives us a way to retrieve the link for a single font, multiple fonts, or multiple fonts with the `font-weight` and `font-style` properties.

A single linked font: 
```html
<head>
  <link href="https://fonts.googleapis.com/css?family=Droid+Serif" type="text/css" rel="stylesheet">
</head>
```

Multiple Linked Fonts:
```html
<head>
  <link href="https://fonts.googleapis.com/css?family=Droid+Serif|Playfair+Display" type="text/css" rel="stylesheet">
</head>
```

Multiple linked fonts along with weights and styles:
```html
<head>
  <link href="https://fonts.googleapis.com/css?family=Droid+Serif:400,700,700i|Playfair+Display:400,700,900i" rel="stylesheet">
</head>
```

#### FONT FACE

To load fonts with the `@font-face` property:

1. Instead of using the font's link in the HTML document, enter the link into the URL bar in the browser.
1. The browser will load the CSS rules. You will need to focus on the rules that are directly labeled as `/* latin */`. Some of the latin rules are on separate lines. You will need each of these.
1. Copy each of the CSS rules labeled latin, and paste the rules from the browser to the top of style.css.

_It important to stress the need to copy the `@font-face` rules to the top of the stylesheet for the font to load correctly in the project._

We can modify our @font-face rule to use local font files as well:

```css
@font-face {
  font-family: "Roboto";
  src: url(fonts/Roboto.woff2) format('woff2'),
       url(fonts/Roboto.woff) format('woff'),
       url(fonts/Roboto.tff) format('truetype');
}
```

1. The main difference is the use of a relative filepath instead of a web URL.
1. We add a format for each file to specify which font to use. Different browsers support different font types, so providing multiple font file options will support more browsers.

As of now .woff2 appears to be the way of the future, due to greatly reduced file sizes and improved performance, but many browsers still don’t support it. There are lots of great sources to find fonts to use locally, such as Font Squirrel (https://www.fontsquirrel.com/).

##### Review
* _Typography_ is the art of arranging text on a page.
* Text can appear in any number of weights, with the `font-weight` property.
* Text can appear in italics with the `font-style` property.
* The vertical spacing between lines of text can be modified with the `line-height` property.
* _Serif_ fonts have extra details on the ends of each letter. _Sans-Serif_ fonts do not.
* _Fallback fonts_ are used when a certain font is not installed on a user's computer.
* Google Fonts provides free fonts that can be used in an HTML file with the `<link>` tag or the `@font-face` property.
* Local fonts can be added to a document with the `@font-face` property and the path to the font's source.

### DESIGN - TYPOGRAPHY

#### FONT PAIRING

The following resources provide in-depth advice on pairing fonts:

1. Typewolf (https://www.typewolf.com/google-fonts)
1. Google Font Combinations (https://www.behance.net/gallery/35768979/Typography-Google-Fonts-Combinations)
1. Hand-picked Tales from Æsop's Fables with Hand-picked Type from Google Fonts (https://femmebot.github.io/google-type/)

#### LEADING AND TRACKING

Leading and tracking are tools to help make sure your text is readable. Leading is the spacing between lines of text. Using the CSS property `line-height`, you can make sure your lines are not crammed together or too far apart. Give the user space to breathe while reading each line.

Tracking is the space between letters throughout a word. While many fonts should have this spacing well designed for great user experience, you may want to adjust slightly to help with the rest of the feel of your site by using the `letter-spacing` CSS property. Most well-made fonts will not need this adjustment though, so use sparingly if at all.

## DAY THREE
### CSS PSEUDO-CLASSES

There may be times when we want to target an element based on the current state of the element or where the element exists on a page. We can do this with pseudo-class selectors. _Pseudo-class selectors_ allow us to style selected elements when they meet certain requirements based on user interactions and context within a web document.

#### PSEUDO CLASS SYNTAX

Generally speaking, pseudo-class selectors:

1. Begin with a colon and are placed at the end of a selector with no spaces before them
1. Are often preceded by a traditional selector, such as `#banner`, `.links`, `header`, or `ul` `li`.

#### DYNAMIC PSEUDO CLASSES

There are a number of other pseudo-classes we can use to target elements based on user interaction. These are often referred to as dynamic pseudo-classes, and the most common ones are:

1. `:link` to style an unvisited link.
1. `:visited` to style a visited link.
1. `:hover` to style an element when a user hovers over the element with the cursor.
1. `:active` to style an element when a user activates an element. This is the time between when a user clicks an element and when they release the mouse.

#### FIRST-CHILD & LAST-CHILD
A common use of pseudo-classes is to style elements based on their context within the HTML document. We often refer to these pseudo classes as _structural pseudo classes_. Imagine you have several elements nested under a parent element, and you want the first element to be styled differently from the rest. Structural pseudo-classes can be helpful.

We'll begin with the `:first-child` pseudo-class selector, which targets elements that are the first child of a parent element.

Similar to the `:first-child` pseudo-class, the `:last-child` pseudo-class targets the last child of a parent element.

#### NTH CHILD
The `nth-child` selector allows us to specify subsets of child elements we want to style, such as every even element, every third element, and so on. When using `nth-child` selectors, we must provide information about what pattern of elements we want to select.

The pattern `nth-child` uses is in the form of `an + b`

1. `a` represents the multiple of elements we want to select. If we want to select every second element, we would set a to 2. If we wanted to select every third element, we would set `a` to `3`.
1. `n` represents a set of zero and increasing positive integers. It is not the element that is selected. The selected element is the result of `a x n + b`.
1. `b` represents the first element we want to start the subset on. If we want to start styling on the third child, we would set b to 3.

For example:

* `a:nth-child(2n + 3)` selects every second link, starting with the third link.
* `a:nth-child(3n + 4)` selects every third link, starting with the fourth link.

`nth-child` syntax for `an + b` at times omits specifications for `b`, or uses `0` in place of `b` as the item to start from. For example, you may see the following code:

`a:nth-child(4n + 0)`

If `b` is of value `0` or is not specified, we will start on element `0`. Since this is not a real element, our first styled element will be on the next interval specified by a.

In the example above, we would style every fourth element, starting on the fourth element.

We can also use the 1 selector to select all even or odd elements under a parent element.

`a:nth-child(even)`

By specifying `even` or `odd`, we can style either even or odd child elements, respectively.