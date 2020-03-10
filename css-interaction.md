# Interaction in CSS

The simplest interactions you can code in CSS are for link hover effects. These use **pseudoclasses** to represent the different link states. Pseudoclasses are written by adding a colon (`:`) and then the pseudoclass to any selector, like so:

```css
a:hover {} /* For when a link is hovered over */
a:focus {} /* For when a link is focused on via keyboard or touchscreen */
a:active {} /* For when a link is clicked */
a:visited {} /* For when a link has previously been clicked */
```

Note that there is **no** space between the selector, colon or pseudoclass; it needs to be all smooshed together.

The "active" state passes by rather quickly, but it can definitely be helpful to provide styles for the other states and you can even combine them, like [this example](https://codepen.io/angeliquejw/pen/vYOppdV?editors=0100).

Sometimes it's painful or frustrating to test pseudoclasses like this in the browser developer tools. Helpfully, most browsers have a way to "lock in" a pseudostate for testing purposes; see the following instructions/details:

- [Google Chrome](https://developers.google.com/web/tools/chrome-devtools/css#pseudostates)
- [Mozilla Firefox](https://developer.mozilla.org/en-US/docs/Tools/Page_Inspector/How_to/Examine_and_edit_CSS)

## Transitions

You can make your hover effects smoother by applying a CSS property called [`transition`](https://developer.mozilla.org/en-US/docs/Web/CSS/transition). See [this CodePen](https://codepen.io/angeliquejw/pen/abOEEYL?editors=0100) to understand the difference `transition` makes in hover effects.

`transition` is what's known as a **shorthand property** -- it's a way to take a handful of CSS properties and smoosh them together in one rule. In the case of `transition`, it combines rules for:
- which properties should be affected
- how long the transition should last
and a few other things into one rule. Handy! (Note, you can always use the individual rules if it's easier for you to understand.)

```css
/* shorthand version */
a {
  transition: all 300ms;
}
/* longer way of saying the same thing */
a {
  transition-property: all;
  transition-duration: 300ms;
}
```

In the above rule, the transition will be applied to _all_ properties and will last for 300ms. Note that on its own, this rule does nothing; it needs to also be combined with a hover effect or other state change. You still control your effects via other CSS properties -- `transition` is just handling how those changes act.

In this example, there's a state change which includes two properties -- `background-color` and `color` both change on hover -- but _only_ `color` will have the transition applied:

```css
a {
  color: red;
  transition: color 300ms;
}
a:hover {
  background-color: red;
  color: white;
}
```

If the code was changed like so:

```css
a {
  color: red;
  transition: all 300ms;
}
a:hover {
  background-color: red;
  color: white;
}
```

then both the `background-color` and `color` will be affected by the transition rule.

Note that you should always apply your `transition` rule to the base element; not the pseudoclass. This makes your code more robust and more likely to act the way you expect.

There are many other options and tweaks you can make using `transition`, but this is enough to get you started and make your hover effects look nicer. 👍

---

[↤ back](README.md#table-of-contents)
