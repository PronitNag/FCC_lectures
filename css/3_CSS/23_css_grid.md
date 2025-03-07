# CSS Grid Notes

## What Is CSS Grid, and How Does It Differ from Flexbox?
CSS Grid is a layout system designed for two-dimensional layouts, allowing control over both rows and columns. Flexbox, on the other hand, is a one-dimensional layout system used for arranging items in a row or column.

### Example:
```css
.container {
  display: grid;
  grid-template-columns: 100px 200px auto;
}
```

## How Can You Create Flexible Grids with the `fr` Unit?
The `fr` (fractional) unit distributes space within a grid, making it flexible.

### Example:
```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
}
```

## How Can You Create Gaps Between Tracks in a Grid?
Use the `gap` property to set space between grid items.

### Example:
```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
}
```

## How Can You Repeat Track Listings in a Grid Layout?
The `repeat()` function allows track definitions to be repeated easily.

### Example:
```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
```

## What Is the Difference Between an Implicit and Explicit Grid?
- **Explicit Grid**: Defined by `grid-template-rows` and `grid-template-columns`.
- **Implicit Grid**: Created automatically when items are placed outside the defined grid.

### Example:
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
.item {
  grid-column: 3; /* Implicit grid */
}
```

## What Is the `minmax()` Function and How Does It Work?
The `minmax(min, max)` function defines a track with a flexible range between a minimum and maximum size.

### Example:
```css
.container {
  display: grid;
  grid-template-columns: minmax(100px, 1fr) 2fr;
}
```

## How Do the `grid-column` and `grid-row` Properties Work?
These properties define how many columns or rows an item should span.

### Example:
```css
.item {
  grid-column: 1 / 3; /* Spans from column 1 to 3 */
  grid-row: 2 / 4;    /* Spans from row 2 to 4 */
}
```

## How Can You Position Items on the Grid Using the `grid-template-areas` Property?
This property allows named areas for easier placement of items.

### Example:
```css
.container {
  display: grid;
  grid-template-areas: 
    "header header"
    "sidebar content"
    "footer footer";
}
.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.content { grid-area: content; }
.footer { grid-area: footer; }

