# Block vs. inline elements

We discussed this a bit last week, but to review, HTML elements are either:

- *block elements* that _always_ start on a new line and take up the full width of that line; or
- *inline elements* that do _not_ start on a new line and only take up as much width as their content.

You can see examples of some of the HTML elements you've already learned [here](https://cdpn.io/angeliquejw/debug/BaNrzWW); adding background colors and borders to the elements makes it obvious which stretch out to the full width (and are block elements) and which do not (and are inline elements).

You can also use your browser's developer tools to sort this out.

So, back to `div` and `span` -- you need to think about how you're going to use the element/container. If you want it to act like an inline element, make it a `span`. Otherwise, go for the `div`.

## Changing the defaults

Just because an element has a default setting of block or inline doesn't mean we're stuck with that. The CSS property `display` can be used to change an element's behavior.

```css
h1 {
  display: inline;
}

span {
  display: block;
}
```
The above CSS forces those elements to act counter to their default settings. Note that you should generally avoid simply reversing the `display` value of a `div` or `span`, as I've done here -- instead, just use the proper element to start with and save yourself writing the extra CSS 👍

There are many more options for the `display` property, but first let's learn a bit more about how CSS affects an element based on if it is inline or block. To do this, let's start to talk about [spacing in CSS](css-spacing.md).

---

[↤ back](README.md#table-of-contents)
