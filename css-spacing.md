# CSS spacing

## Margin and padding

As may have been evident from earlier examples, essentially everything in HTML is, essentially, a box. A `div` is a box, a `p` is a box.

When we think about spacing in CSS, you have to consider if you want the spacing to occur either _inside_ or _outside_ of that box.

`padding` is the CSS property for spacing within the element's box; `margin` is the property for spacing outside of the box.

```css
  p {
    background-color: thistle;
    margin: 10px;
    padding: 10px;
  }
```

The above CSS results in a `p` element that has a background color that covers the entire element/box. There's 10 pixels of padding on each side of the box (top, right, bottom and left), so the background color extends an extra 10 pixels on every side. The 10 pixels of margin is also on each side and pushes the `p` element away from other surrounding elements, but the margin does _not_ extend the background color because it is _outside_ of the box.

Just like `transition`, `margin` and `padding` are shorthand properties.

```css
p {
  margin: 10px;
  margin: 5px 10px 15px 20px;
  margin-top: 5px;
  margin-right: 10px;
  margin-bottom: 15px;
  margin-left: 20px;
}
```

The first rule above (`margin: 10px;`) puts 10 pixels of margin on each side of the box. The second rule adds 5 pixels of margin to the top of the box, 10 pixels to the right side, 15 pixels to the bottom and 20 pixels to the left. The four rules that follow do the same thing, just broken out into individual rules (ie, not using the shorthand).

The shorthand of `margin` and `padding` can take between one to four values:

- One value (`margin: 10px;`) applies the same value to all four sides of the box.
- Two values (`margin: 10px 20px;`) applies the first value to the top and bottom of the box and the second value to the left and right sides of the box.
- Three values (`margin: 10px 5px 20px;`) appies the first value to the top of the box, the middle value to the left and right sides, and th elast value to the bottom of the box.
- Four values (`margin: 5px 10px 15px 20px;`) applies a unique value to each side of the box, starting and the top and going clockwise: top, right, bottom, left.

This is, understandably, fairly confusing, so [here's an example](https://codepen.io/angeliquejw/pen/ZEGxOZP?editors=0100) to investigate and play around with.

If it's overwhelming to you, try this: use the shorthand version for when you have a single value and, otherwise, write out the individual properties (ie, `margin-top`, `padding-left`).

Learn more about:
- [margin](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
- [padding](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)

## Height and width

While `margin` and `padding` give you some control over the size of any HTML element, you can also specifically set a height and width on HTML elements via CSS:

```css
div {
  height: 100px;
  width: 100px;
}
```

The above CSS will result in a `div` that is a 100 pixel square.

`height` and `width` take a variety of values, but sticking to pixels (`px`) and percentages is a good way to start.

For images that may be larger than your browser window, the following CSS will sort you out:

```css
img {
  height: auto;
  width: 100%;
}
```

The `width` rule keeps the image from being larger than its parent container and the `height` rule makes sure the aspect ratio of the image doesn't get skewed 👍

While `width` works as expected in most cases, I want to provide two warnigs about the `height` property:

-  I _highly_ recommend avoiding setting a specific `height` on any HTML element containing text. It is very easy, as users experience your design on different devices or even just shrink their browser windows, to end up with text that escapes a box (see [example](https://codepen.io/angeliquejw/pen/ZEGxpEN?editors=1100)).
- While `width: 100%;` is a fairly easy to understand bit of CSS, `height: 100%;` is rarely the solution to any of your issues.

Learn more about:
- [height](https://developer.mozilla.org/en-US/docs/Web/CSS/height)
- [width](https://developer.mozilla.org/en-US/docs/Web/CSS/width)

## Block vs. inline, part 2

Margin, padding, width and height  work entirely as described and expected for block elements, but inline elements are another story. We can use [this Pen](https://codepen.io/angeliquejw/pen/LYVdZmE) to experiment with that.

The important thing to note is that top and bottom `margin` and `padding` are either wonky or ignored for an inline element; `height` and `width` are _totally_ ignored. If you want the best of both worlds -- an element that doesn't start on a new line _and_ respects top and bottom margins and padding, you need to use a hybrid `display` property:

```css
p {
  display: inline-block;
}
```

The `inline-block` value delivers the best of both worlds and can be relied on to help you solve some of your layout issues.

## Box-sizing

The way an element's height and width is determined in CSS is handled via the `box-sizing` property. `box-sizing` has two possible values

- `content-box`, which is the default that browsers use, where the height, width, padding and border values all combine to determine the element's size. As a result, an element with a height and width of 200px, a 10px border and 50px of padding is not, in fact 200 x 200px, but instead 320 x 320px; consider just the dimensions from top to bottom:
10px border +
50px padding +
200px height +
50px padding +
10px border = 320px
- `border-box` is a better option where the padding and border are included into the height and width, so an element with the same settings as above (height and width of 200px, a 10px border and 50px of padding) is, in fact, 200px.

See [this example](https://codepen.io/angeliquejw/pen/xapWpg?editors=0100) to see the effect of `box-sizing` in action.

In general, I recommend always using `border-box`; you can make sure it is applied to your entire stylesheet by applying it to _every_ eleemnt via the global selector (`*`), like so:

```css
* {
  box-sizing: border-box;
}
```

The global selector is powerful, but shouldn't be overused; this is one of the good examples of using it.

---

[↤ back](README.md#table-of-contents)
