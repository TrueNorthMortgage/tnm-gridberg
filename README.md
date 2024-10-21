## About Gridberg ##

Gridberg is an ultra light-weight css boilerplate and library. Built with SASS, Gridberg's set of configurable variables allow you to build a custom grid system, with any number of columns, and any number of breakpoints. All in just a few keystrokes.

It is recommend that you put all your own styles into the scss file where you will be importing gridberg.

A vanilla compiled Gridberg file weighs in at just 5kb.

### Implementation ###

Copy the following configuration into the top of the main scss file for your project.

```
/* Your Build: */
/* Set the number of columns in your grid */
$total-columns: 12;
/* Set your breakpoints in px, add as many as you like. */
$breakpoints: (
    large: 1000px,
    medium: 767px,
    smedium: 700px,
    small: 600px
);
/* Set the default padding for your columns */
$column-padding-right: 10px;
$column-padding-left: 10px;

/* Load Gridberg */
@import 'PROJECT_ROOT/node_modules/@pump/gridberg/scss/gridberg.scss';
```

### Classes To Know ###

Use these classes on your HTML elements:

`.col-(breakpoint label)-(number for width of column)-($total-columns)`: Set a column width, usually you add this class to a div.

`.grid`: Optionally, you can wrap your columns in a grid wrapper. It will get a negative margin from your left and right column padding. This means you don't need psuedo-selectors on your columns, or extra classes.

`.kill-the-padding`: sets your column to 0px padding, this can be overwritten through using a custom column class like .col-f-lp.

`.img-responsive`: makes an image display: block, width: 100%, height: auto.

`.disable-scrolling`: overflow: hidden an element.

### Helpers ###

Use these helpers in your ‘my.scss’ file:

`@mixin clearfix`: Clear the parent of floated objects like columns (to get the correct height).

`@mixin img-responsive`: Makes an image responsive, consider adding max-width to the image as well.

`@mixin text-percent()`: Converts px font-size to %, 16(px) == 100%.

`@mixin text-rem()`: Converts px font-size to rem, 16(px) == 1rem.

`@mixin inner`: place on an inner div center and set a max width matching your 1st break point.

`@mixin flex`: Display an element as flexbox.

`@mixin flex-wrap`: Display an element as a flexbox with wrapping items.
