Active learning: mobile first responsive design

```
@media media-type and (media-feature-rule) {
  /* CSS rules go here */
}
```

The width (and height) media features can be used as ranges, and therefore be prefixed 
with min- or max- to indicate that the given value is a minimum, or a maximum. For 
example, to make the color blue if the viewport is 600 pixels or narrower, use max-width:

```
@media screen and (max-width: 600px) {
  body {
    color: blue;
  }
}
```

One well-supported media feature is orientation, which allows us to test for portrait or 
landscape mode. To change the body text color if the device is in landscape orientation, 
use the following media query.

```css
@media (orientation: landscape) {
  body {
    color: rebeccapurple;
  }
}
```

<p>Or,</p>

```css
@media not (orientation: landscape) {
  body {
    color: blue;
  }
}
```

As part of the Level 4 specification, the hover media feature was introduced. This feature 
means you can test if the user has the ability to hover over an element, which essentially 
means they are using some kind of pointing device; touchscreen and keyboard navigation 
does not hover.

```css
@media screen and (hover: hover) {
  body:hover {
    color: white;
    background: black;
  }
}
```

One common case is to check if the viewport width is between two values:


```css
@media (min-width: 30em) and (max-width: 50em) {
  /* … */
}
```

If you want to improve the readability of this, you can use "range" syntax:

```css
@media (30em <= width <= 50em) {
  /* … */
}
```
