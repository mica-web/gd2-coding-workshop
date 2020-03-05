# Best practices to _avoid_ problems with your code

- **Save often, test often.** It's much harder to troubleshoot code if you've made many changes and don't know when or where the problem was introduced. Get into the habit of saving after you add a few lines of code and previewing the results.
- **Organize your code.** Organizing your code makes it so much easier to find issues. 
 - In HTML, use consistent linebreaks and proper indentation for nested elements.

Example of disorganized HTML:
```html
<div><h1>Hello</h1><ul><li>This is a list item</li><li>Another item</li></ul></div>
```

```html
<div>
  <h1>Hello</h1>
  <ul>
    <li>This is a list item</li>
    <li>Another item</li>
  </ul>
</div>
```
Whitespace is free, so make your code readable 😁

 - In CSS, do the same, but also consider using comments to break up sections and make the code organization apparent. You can also alphabetize by property, which helps prevent issues with duplicate properties conflicting and causing confusion. [See example of well-organized CSS.](examples/organized-code.css)


# Troubleshooting

If your code is broken or not working as you expected, try the following:

- **Take a break.** - My #1 piece of advice. Sometimes, you just need a break. 🚶‍♀️
- **Organize your code.** Fix your indentation and alphabetize your CSS properties if they've gotten sloppy. 🧹
- **Identify the problem.** - Take your time and look at your code again. First, try to find what is causing the problem. Which area of the page do you see the problem? Go to the same section in HTML and CSS. Look for any mistakes. If you're still struggling, go over your code slowly line by line and see if you missed any brackets, parentheses, colons, semicolons, etc. Remember that the editor may provide some hints. 🔍
- **Isolate the problem.** - Use HTML comments `<!-- -->` and CSS comments `/* */` to isolate the problem. Try adding comments to different blocks of code so that the browser will skip the commented area. If the problem goes away, then the problem must be somewhere within the commented section. 🔲
- **Have another person look at your code.** - More often than not, it is a small mistake that is causing the problem. Ask your classmate to look over your code. They will provide a fresh view. 👀
- **Start a new file.** - Open up an empty page and retype -- _NOT_ copy and paste -- the problematic code block. See if you can recreate the problem. If you can, focus on that code block only. 🆕

---

[↤ back](README.md#table-of-contents)
