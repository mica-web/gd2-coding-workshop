# HTML container elements

In addition to elements that wrap around text, sometimes it is useful to have other HTML elements to wrap around those elements, joining them togther so, for example, your heading and the paragraphs under it all have the same background color.

It's best to add container elements on an as-needed basis -- not every web page needs each of these elements.

## Semantic

![HTML5 container elements](img/html5-container-elements.png)

Some of the container elements are meaningful and represent the organization of a page.
- [`main`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main) represents the main content of a page; a page should only have one `main` element and it should include content unique to the page.
- In comparison, the following elements often include content that is repeated across the pages of a site:
  - [`header`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header) is for introductory content
  - [`nav`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav) contains the major navigation links for a site
  - [`aside`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside) is a container for content that is related to the content within `main`
  - [`footer`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer) contains details about its parent element (for example, the copyright details for a page or the author section on a blog post or article).

- [`section`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section) is used if and when you need to break down the content inside a `main` or other element even further (so, a blog post with mutiple headings and content sections could use this). Again, only use `section` if you need it after starting to apply your CSS/styles.

The other elements you've already learned can be nested inside these container elements. See [this example](examples/container-elements.html).

## Generic
While it's best to use a semantic element, something that adds meaning to your document, sometimes there's no right choice from the existing elements. In those cases, there are two generic container elements that give no extra meaning to your HTML document: `div` and `span`.

To understand when to use `div` or `span`, you need to understand [box vs inline elements](inline-vs-block.md).

---

[↤ back](README.md#table-of-contents)
