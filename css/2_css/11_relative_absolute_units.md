# CSS Units and calc() Function

## Absolute Units in CSS

Absolute units in CSS are fixed and do not change based on the parent element or viewport. They are best used when you need precise control over an element’s size.

### Common Absolute Units:
- `px` (pixels) - Most commonly used.
- `cm` (centimeters)
- `mm` (millimeters)
- `in` (inches)
- `pt` (points, 1pt = 1/72 of an inch)
- `pc` (picas, 1pc = 12pt)

### Example:
```css
.box {
  width: 200px;
  height: 100px;
  background-color: lightblue;
}
```

### When to Use Absolute Units:
- When exact sizes are required (e.g., print stylesheets, fixed-size components).
- Avoid using them for responsive designs.

---

## Percentages in CSS

Percentage values in CSS are relative to the parent element’s size.

### Example:
```css
.container {
  width: 500px;
}
.child {
  width: 50%; /* 50% of the parent's width (500px) */
  background-color: yellow;
}
```

### When to Use Percentages:
- When creating fluid layouts.
- For elements that should adjust based on their container size.

---

## ems and rems in CSS

- `em` is relative to the font size of the parent element.
- `rem` (root em) is relative to the root (`html`) font size.

### Example:
```css
html {
  font-size: 16px;
}
.container {
  font-size: 20px;
}
.child {
  font-size: 2em; /* 2 * 20px = 40px */
}
.another-child {
  font-size: 2rem; /* 2 * 16px = 32px */
}
```

### When to Use ems and rems:
- Use `rem` for global font scaling.
- Use `em` for local component-based scaling.

---

## vh and vw Units

- `vh` (viewport height) - 1vh is 1% of the viewport height.
- `vw` (viewport width) - 1vw is 1% of the viewport width.

### Example:
```css
.fullscreen {
  width: 100vw;
  height: 100vh;
  background-color: green;
}
```

### When to Use vh and vw:
- When designing elements that should take up the full viewport.
- For responsive layouts where element sizes depend on the screen size.

---

## The calc() Function in CSS

`calc()` allows mathematical calculations within CSS properties.

### Example:
```css
.box {
  width: calc(100% - 50px);
  height: calc(50vh + 20px);
  background-color: red;
}
```

### How calc() Works:
- Allows addition (`+`), subtraction (`-`), multiplication (`*`), and division (`/`).
- Useful for dynamic layouts where fixed and flexible values need to be combined.

### When to Use calc():
- When mixing different units.
- When making precise adjustments to layout without media queries.

