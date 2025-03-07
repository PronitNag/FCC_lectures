# Design Basics

## Common Design Terms
Understanding design terminology helps in effective communication with designers.

- **Typography**: The style and appearance of text.
- **Contrast**: The difference between elements to create visual interest.
- **Hierarchy**: Arranging elements to show importance.
- **Alignment**: Positioning elements for a structured look.
- **Whitespace**: Empty spaces that improve readability.

```css
/* Example of typography styling */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}
```

## Background and Foreground Contrast
Good contrast ensures readability and accessibility.

- Use high contrast between text and background.
- Avoid using similar colors that blend together.
- Test designs in grayscale to check contrast effectiveness.

```css
/* Example of good contrast */
.text {
    color: #ffffff;
    background-color: #333333;
}
```

## Importance of Visual Hierarchy
Visual hierarchy guides the user’s eye through content.

- Use size, color, and spacing to emphasize important elements.
- Headlines should be larger and bolder than body text.

```html
<h1>Main Heading</h1>
<p>Supporting text with less emphasis.</p>
```

## Scale in Design
Scale creates emphasis and balance in a design.

- Larger elements attract more attention.
- Scale should be used consistently to maintain harmony.

```css
h1 {
    font-size: 2em;
}
small {
    font-size: 0.8em;
}
```

## Alignment in Design
Alignment brings structure and order to layouts.

- Left-aligned text is easier to read.
- Center alignment works well for short text blocks.

```css
.text-left {
    text-align: left;
}
.text-center {
    text-align: center;
}
```

## Importance of Whitespace
Whitespace improves clarity and prevents clutter.

- Increases readability.
- Separates elements to improve focus.

```css
.container {
    padding: 20px;
}
```

## Best Practices for Working with Images
Using images effectively enhances design.

- Optimize images for web to reduce load time.
- Use alternative text for accessibility.
- Ensure images complement the design style.

```html
<img src="image.jpg" alt="Description of image" width="300" height="200">
```

## Progressive Enhancement
Progressive enhancement ensures functionality across all devices.

- Start with a basic version and enhance with additional features.
- Improves accessibility and user experience.

```html
<button>Click Me</button>
<noscript>Your browser does not support JavaScript.</noscript>
```

By following these design principles, you can create visually appealing and user-friendly designs.

