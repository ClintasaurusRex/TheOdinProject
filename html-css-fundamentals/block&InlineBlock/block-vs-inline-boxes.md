# Block and Inline Boxes in CSS

## Table of Contents

- [Introduction](#introduction)
- [Block Boxes](#block-boxes)
  - [Block Box Example](#block-box-example)
- [Inline Boxes](#inline-boxes)
  - [Inline Box Example](#inline-box-example)
- [Block vs Inline: Key Differences](#block-vs-inline-key-differences)
- [Changing Display Types](#changing-display-types)
- [Summary](#summary)
- [References](#references)

---

## Introduction

In CSS, every element on a web page is a rectangular box. These boxes are either **block** or **inline** by default, and their type affects how they behave in the layout. Understanding the difference between block and inline boxes is fundamental for controlling your page's structure and appearance.

---

## Block Boxes

**Block-level elements** (block boxes) start on a new line and stretch out as far as they can horizontally. They stack vertically, one after another.

**Common block elements:**  
`<div>`, `<p>`, `<h1>`, `<ul>`, `<li>`, `<section>`, `<article>`

### Block Box Example

```html
<div style="background: #cce5ff; padding: 10px;">This is a block-level element.</div>
<p style="background: #d4edda; padding: 10px;">This is another block-level element.</p>
```

**Result:**  
Each element appears on its own line, taking up the full width available.

---

## Inline Boxes

**Inline elements** (inline boxes) do not start on a new line. They only take up as much width as necessary and flow alongside other inline elements within the same line.

**Common inline elements:**  
`<span>`, `<a>`, `<strong>`, `<em>`, `<img>`

### Inline Box Example

```html
<p>
  This is a <span style="background: #fff3cd;">highlighted</span> word in a sentence.
  <a href="#" style="background: #f8d7da;">This is a link</a> in the same line.
</p>
```

**Result:**  
The `<span>` and `<a>` elements appear within the same line as the surrounding text.

---

## Block vs Inline: Key Differences

| Feature            | Block Elements         | Inline Elements             |
| ------------------ | ---------------------- | --------------------------- |
| Starts on new line | Yes                    | No                          |
| Width              | Fills available width  | Only as wide as content     |
| Height             | Can set width/height   | Ignores width/height        |
| Margin/Padding     | All sides respected    | Only left/right respected   |
| Examples           | `<div>`, `<p>`, `<h1>` | `<span>`, `<a>`, `<strong>` |

---

## Changing Display Types

You can change an element's box type using the `display` property in CSS:

```css
span {
  display: block; /* Makes an inline element behave like a block */
}

div {
  display: inline; /* Makes a block element behave like inline */
}
```

---

## Summary

- **Block elements** stack vertically and take up the full width.
- **Inline elements** flow horizontally and only take up as much space as needed.
- You can change an element's display type with CSS.

---

## References

- [MDN: Box model basics](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics/Box_model)
