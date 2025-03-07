# Fundamentals of Typography

Typography is the art and technique of arranging type to make written language legible, readable, and visually appealing. It involves selecting typefaces, point sizes, line lengths, line-spacing (leading), and letter-spacing (tracking and kerning).

## Key Elements:
- **Typeface & Fonts**: A typeface is a family of related fonts. A font is a specific style within a typeface (e.g., Arial Bold).
- **Line Spacing (Leading)**: The vertical space between lines of text.
- **Kerning**: The adjustment of space between individual characters.
- **Tracking**: The adjustment of space between groups of letters.
- **Alignment**: Left, right, center, and justified text alignment.

```css
p {
  font-family: 'Arial', sans-serif;
  line-height: 1.5;
  letter-spacing: 0.05em;
  text-align: justify;
}
```

# Best Practices for Typography in Design

1. **Use Readable Fonts** – Stick to legible and clear fonts for better accessibility.
2. **Limit the Number of Fonts** – Use a maximum of 2-3 fonts per design.
3. **Maintain Proper Contrast** – Ensure sufficient contrast between text and background.
4. **Consistent Line Spacing** – Use appropriate line height for readability.
5. **Avoid Distorting Fonts** – Never stretch or squeeze fonts.

```css
h1 {
  font-family: 'Georgia', serif;
  font-size: 2rem;
  color: #333;
}
```

# Font Families and How They Work

Font families define groups of fonts that share similar design characteristics. Common types include:

- **Serif**: Fonts with small strokes at the end of letters (e.g., Times New Roman).
- **Sans-serif**: Clean fonts without strokes (e.g., Arial, Helvetica).
- **Monospace**: Every letter takes up the same width (e.g., Courier New).
- **Cursive**: Fonts that resemble handwriting (e.g., Brush Script).
- **Fantasy**: Decorative fonts used for special effects.

```css
body {
  font-family: 'Courier New', monospace;
}
```

# Web Safe Fonts

Web safe fonts are fonts that are available on most operating systems and browsers. Some common web-safe fonts include:

- Arial, Helvetica (Sans-serif)
- Times New Roman, Georgia (Serif)
- Courier New (Monospace)
- Verdana, Tahoma (Sans-serif)

```css
body {
  font-family: Arial, sans-serif;
}
```

# @font-face At-Rule

The `@font-face` rule allows developers to load custom fonts from external sources and use them in web pages.

```css
@font-face {
  font-family: 'MyCustomFont';
  src: url('fonts/myfont.woff2') format('woff2'),
       url('fonts/myfont.woff') format('woff');
}

h1 {
  font-family: 'MyCustomFont', sans-serif;
}
```

# External Fonts (Google Fonts & Font Squirrel)

You can use external font services like Google Fonts and Font Squirrel to include stylish fonts in your design.

**Using Google Fonts:**
```html
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
```
```css
body {
  font-family: 'Roboto', sans-serif;
}
```

# text-shadow Property

The `text-shadow` property adds a shadow effect to text.

```css
h1 {
  text-shadow: 2px 2px 5px rgba(0,0,0,0.5);
}
```

**Syntax:**
```css
text-shadow: horizontal-offset vertical-offset blur-radius color;
```
Example:
```css
h2 {
  text-shadow: 3px 3px 6px #666;
}

