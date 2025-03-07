# CSS Flexbox Notes

## What Is CSS Flexbox, and When Should You Use It?

CSS Flexbox (Flexible Box) is a layout model designed to arrange items within a container efficiently, even when their sizes are unknown or dynamic. It provides an easy way to distribute space and align items in a container.

### When to Use Flexbox?
- When you need a one-dimensional layout (either row or column).
- When items need to be evenly spaced or dynamically resized.
- When aligning items is a challenge with traditional CSS methods.
- When creating responsive designs without using floats or positioning.

### Example:
```css
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 200px;
    border: 1px solid black;
}
.item {
    width: 100px;
    height: 100px;
    background-color: lightblue;
}
```
```html
<div class="container">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
</div>
```

## What Are Some Common Flex Properties, and How Do They Work?

### 1. `display: flex;`
This makes an element a flex container, enabling flex behavior for its children.

### 2. `flex-direction`
Defines the direction in which flex items are placed.
- `row` (default) → Left to right
- `column` → Top to bottom
- `row-reverse` → Right to left
- `column-reverse` → Bottom to top

```css
.container {
    display: flex;
    flex-direction: column;
}
```

### 3. `justify-content`
Aligns items along the main axis.
- `flex-start` → Items align at the start
- `flex-end` → Items align at the end
- `center` → Items are centered
- `space-between` → Space between items
- `space-around` → Space around items

```css
.container {
    display: flex;
    justify-content: center;
}
```

### 4. `align-items`
Aligns items along the cross axis.
- `flex-start`, `flex-end`, `center`, `baseline`, `stretch`

```css
.container {
    display: flex;
    align-items: flex-end;
}
```

### 5. `flex-wrap`
Defines if items should wrap or stay in a single line.
- `nowrap` (default)
- `wrap` → Wrap to the next line
- `wrap-reverse` → Wrap in reverse order

```css
.container {
    display: flex;
    flex-wrap: wrap;
}
```

### 6. `flex`
A shorthand for `flex-grow`, `flex-shrink`, and `flex-basis`.

```css
.item {
    flex: 1;
}
```

### 7. `align-self`
Allows individual items to override `align-items`.

```css
.item:nth-child(2) {
    align-self: center;
}
```

These are the basic properties that will help you understand and use Flexbox efficiently in CSS.
