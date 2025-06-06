# Block and Inline Boxes in CSS

## Table of Contents

- [Introduction](#introduction)
- [Block Boxes](#block-boxes)
  - [Block Box Example](#block-box-example)
- [Inline Boxes](#inline-boxes)
  - [Inline Box Example](#inline-box-example)
- [Block vs Inline: Key Differences](#block-vs-inline-key-differences)
- [Inner and Outer Display Types](#inner-and-outer-display-types)
- [Using display: inline-block](#using-display-inline-block)
- [Summary](#summary)
- [References](#references)

---

## Introduction

In CSS, every element is a box. These boxes are either block or inline by default, and their type affects how they behave in the layout. Understanding block and inline boxes is essential for controlling your page's structure and appearance.

---

## Block Boxes

A box with `display: block`:

- Breaks onto a new line.
- Respects width and height properties.
- Padding, margin, and border push other elements away from the box.
- If width is not specified, it fills the available space in its container.

**Common block elements:** `<div>`, `<p>`, `<h1>`, `<ul>`, `<li>`, `<section>`, `<article>`

### Block Box Example

```html
<div style="background: #cce5ff; padding: 10px; margin-bottom: 10px;">
  This is a block-level element.
</div>
<p style="background: #d4edda; padding: 10px;">This is another block-level element.</p>
```

**Result:** Each element appears on its own line, taking up the full width available.

---

## Inline Boxes

A box with `display: inline`:

- Does not break onto a new line.
- Width and height properties do not apply.
- Top and bottom padding, margins, and borders do not push other elements away, but left and right do.

**Common inline elements:** `<span>`, `<a>`, `<em>`, `<strong>`, `<img>`

### Inline Box Example

```html
<p>
  This is a
  <span style="background: #fff3cd; border: 1px solid #ffc107; padding: 2px 6px;">highlighted</span>
  word in a sentence.
  <a href="#" style="background: #f8d7da; border: 1px solid #f5c6cb; padding: 2px 6px;"
    >This is a link</a
  >
  in the same line.
</p>
```

**Result:** The `<span>` and `<a>` elements appear within the same line as the surrounding text.

---

## Block vs Inline: Key Differences

| Feature            | Block Elements         | Inline Elements             |
| ------------------ | ---------------------- | --------------------------- |
| Starts on new line | Yes                    | No                          |
| Width              | Fills available width  | Only as wide as content     |
| Height             | Can set width/height   | Ignored                     |
| Margin/Padding     | All sides respected    | Only left/right respected   |
| Examples           | `<div>`, `<p>`, `<h1>` | `<span>`, `<a>`, `<strong>` |

---

## Inner and Outer Display Types

- The `display` property has outer and inner display types.
- Outer display type (`block`, `inline`) affects how the box is laid out in relation to other boxes.
- Inner display type (like `flex`, `grid`) affects how children are laid out inside the box.
- Example: `display: flex` makes the element a block box with flex layout for its children.

---

## Using display: inline-block

`display: inline-block` is a special value that combines features of both block and inline elements:

- Does not break onto a new line (like inline).
- Respects width and height (like block).
- Useful for styling inline elements with box properties.

**Example:**

```html
<span
  style="display: inline-block; width: 100px; height: 40px; background: #e2e3e5; border: 1px solid #adb5bd; text-align: center; line-height: 40px;"
  >Inline-block span</span
>
```

---

## Summary

- Block and inline boxes are the foundation of CSS layout.
- Block boxes stack vertically and fill available width.
- Inline boxes flow horizontally and only take up as much space as needed.
- `display: inline-block` offers a middle ground.
- You can change an element's display type with CSS.

---

## References

- [MDN: Box model basics](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics/Box_model)
