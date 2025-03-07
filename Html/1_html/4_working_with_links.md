# Different Target Attribute Types

The `target` attribute in HTML is used with anchor (`<a>`), form (`<form>`), and other elements to specify how the linked content should be opened.

### Common Values:
- `_self`: Default. Opens the link in the same tab.
- `_blank`: Opens the link in a new tab or window.
- `_parent`: Opens the link in the parent frame (used in framesets).
- `_top`: Opens the link in the full body of the window, breaking out of frames.

```html
<a href="https://example.com" target="_blank">Open in new tab</a>
```

# Absolute vs. Relative Paths

### Absolute Path:
- Specifies the full URL or file location from the root directory.
- Starts with `http://`, `https://`, or `/` for server root-based paths.

```html
<img src="https://example.com/images/photo.jpg" alt="Absolute Path Image">
```

### Relative Path:
- Specifies the location relative to the current document.

```html
<img src="images/photo.jpg" alt="Relative Path Image">
```

# Slashes, Single Dot, and Double Dot in Path Syntax

- `/` (Slash): Refers to the root directory.
- `.` (Single Dot): Refers to the current directory.
- `..` (Double Dot): Moves up one directory level.

```html
<!-- Root directory reference -->
<a href="/about.html">About Us</a>

<!-- Current directory reference -->
<img src="./logo.png" alt="Logo">

<!-- Move up one level -->
<a href="../index.html">Go to Home</a>
```

# Different Link States and Their Importance

Links have different states in CSS, which help improve user experience:

### Common Link States:
- `a:link` → Default, unvisited link.
- `a:visited` → A link that has been visited.
- `a:hover` → When a user hovers over the link.
- `a:active` → When the link is clicked.

```css
a {
  color: blue;
}

a:visited {
  color: purple;
}

a:hover {
  color: red;
}

a:active {
  color: green;
}
```

Using these states ensures better navigation and accessibility for users.
