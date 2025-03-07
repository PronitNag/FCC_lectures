# CSS Concepts Notes

## What Is Overflow in CSS, and How Does It Work?
The `overflow` property in CSS controls how content is displayed when it exceeds the dimensions of its container.

### Values:
- `visible` (default) – Content overflows the container.
- `hidden` – Hides overflowing content.
- `scroll` – Adds a scrollbar.
- `auto` – Adds a scrollbar only when needed.

```css
.box {
  width: 200px;
  height: 100px;
  overflow: hidden;
}
```

## What Is the CSS Transform Property, and How Does It Work?
The `transform` property allows applying transformations like rotation, scaling, skewing, and translation to an element.

### Example:
```css
.box {
  transform: rotate(45deg);
}
```

Common transformations include:
- `rotate(deg)` – Rotates an element.
- `scale(x, y)` – Resizes an element.
- `translate(x, y)` – Moves an element.
- `skew(x, y)` – Skews an element.

## What Is the CSS Box Model, and How Does It Work?
The CSS Box Model describes how elements are structured in terms of content, padding, border, and margin.

### Box Model Components:
1. **Content** – The actual content of the element.
2. **Padding** – Space inside the border.
3. **Border** – Surrounds padding and content.
4. **Margin** – Space outside the border.

```css
.box {
  width: 100px;
  padding: 10px;
  border: 5px solid black;
  margin: 20px;
}
```

## What Is Margin Collapsing, and How Does It Work?
Margin collapsing occurs when vertical margins of adjacent elements combine into a single margin instead of adding up.

### Example:
```css
.div1 {
  margin-bottom: 20px;
}

.div2 {
  margin-top: 30px;
}
```
The resulting margin between `.div1` and `.div2` will be **30px** (larger of the two), not 50px.

## What Is the Difference Between content-box and border-box?
The `box-sizing` property determines how the total width and height of an element are calculated.

- **`content-box` (default)** – Width/height includes only content, excluding padding and border.
- **`border-box`** – Width/height includes content, padding, and border.

### Example:
```css
.box-content {
  width: 100px;
  box-sizing: content-box;
}

.box-border {
  width: 100px;
  box-sizing: border-box;
}
```

## What Is a CSS Reset, and What Are Some Common Examples?
A CSS reset removes default browser styles to ensure consistency across different browsers.

### Common CSS Reset:
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```
Other resets include **Normalize.css** and **Eric Meyer's Reset CSS**.

## What Is the CSS Filter Property, and What Are Common Examples?
The `filter` property applies visual effects like blur, brightness, contrast, etc., to elements.

### Example:
```css
img {
  filter: grayscale(100%);
}
```

### Common Filters:
- `blur(px)` – Blurs the element.
- `brightness(%)` – Adjusts brightness.
- `contrast(%)` – Adjusts contrast.
- `grayscale(%)` – Converts to grayscale.
- `sepia(%)` – Applies a sepia tone.

---
Save this file in your GitHub repository for quick reference!

