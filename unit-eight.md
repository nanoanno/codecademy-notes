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

