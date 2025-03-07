# CSS Positioning and Floats

## 1. What Are Common Use Cases for Using Floats, and How Do They Work?

Floats are used to position elements horizontally by taking them out of the normal document flow. They are commonly used for:
- Creating layouts (before Flexbox and Grid)
- Wrapping text around images
- Floating navigation bars

### Example:
```css
img {
  float: right;
  margin: 10px;
}
```
```html
<p>This is an example text. <img src="image.jpg" alt="Example"> The text wraps around the image.</p>
```

## 2. What Is Relative Positioning, and How Does This Differ from the Default Static Positioning?

**Static positioning** is the default position of elements (not affected by `top`, `left`, `right`, or `bottom`).

**Relative positioning** moves an element relative to its original position without affecting the layout of other elements.

### Example:
```css
div {
  position: relative;
  top: 20px;
  left: 30px;
}
```
```html
<div>This element is moved 20px down and 30px right.</div>
```

## 3. What Is Absolute Positioning, and How Does It Work?

An element with **absolute positioning** is removed from the document flow and positioned relative to the nearest positioned ancestor (not `static`). If no positioned ancestor exists, it is placed relative to the `<html>` element.

### Example:
```css
.container {
  position: relative;
  width: 200px;
  height: 200px;
}
.child {
  position: absolute;
  top: 50px;
  left: 50px;
}
```
```html
<div class="container">
  <div class="child">Absolute Position</div>
</div>
```

## 4. What Is Fixed and Sticky Positioning, and How Does It Differ from Absolute Positioning?

### **Fixed Positioning**
- The element is removed from the normal flow and positioned relative to the viewport.
- It does not move even when scrolling.

### Example:
```css
.fixed-element {
  position: fixed;
  top: 0;
  right: 0;
  background: red;
}
```
```html
<div class="fixed-element">I stay fixed at the top-right</div>
```

### **Sticky Positioning**
- The element acts like `relative` until a scroll threshold is reached, then it sticks like `fixed`.

### Example:
```css
.sticky-element {
  position: sticky;
  top: 20px;
  background: yellow;
}
```
```html
<div class="sticky-element">I stick when scrolling</div>
```

## 5. What Is the Z-Index Property, and How Does It Work to Control the Stacking of Positioned Elements?

**`z-index`** controls the stacking order of elements. Higher values appear in front of lower values.

### Example:
```css
.box1 {
  position: absolute;
  z-index: 1;
  background: blue;
}
.box2 {
  position: absolute;
  z-index: 2;
  background: red;
}
```
```html
<div class="box1">Box 1</div>
<div class="box2">Box 2 (appears above Box 1)</div>
```

---
This document provides a brief overview of CSS positioning and floats. You can use these concepts in layout design effectively!

