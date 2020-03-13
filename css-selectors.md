# CSS selectors

Previously, we mainly wrote CSS by using HTML elements as our selectors, like so:

```css
div {
  background-color: yellow;
}
p {
  margin: 10px;
}
```

This breaks down, however, when you don't want _all_ your `div`s to have that background color or want one specific `p` element to have different styles.

To do this, we can add an attribute to _any_ HTML element, like so:

```html
<p class="intro">This text should look different than other p tags.</p>
```

Now, instead of using `p` as our selector, we can use the classname "intro", like so:

```css
.intro {
  font-size: 36px;
  font-weight: bold;
}
```

These rules will _only_ be applied to elements with the classname "intro".

Some notes about doing this:

- The classname in the HTML and CSS must match exactly; typos or differences in capitalization will cause the CSS not to work as you intend.
  - For this reason, I _highly_ recommend keeping all your classnames lowercase.
- You don't need to add classnames to _everything_, just the things you want to target specifically.
- You _can_ use the same classname on multiple elements. So, if all your artist names have the same style, you can apply the classname "artist-name" to that element and only write the CSS once to update all those elements!

See [this example](https://codepen.io/angeliquejw/pen/dyompMN?editors=1100) to better understand how and when to use classnames.

---

[↤ back](README.md#table-of-contents)
