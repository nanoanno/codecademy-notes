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

