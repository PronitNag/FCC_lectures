# Color Theory and CSS Colors

## What Is Color Theory in Design?
Color theory is a set of guidelines for mixing and combining colors to create visually appealing designs. It includes concepts such as:

- **Primary Colors**: Red, Blue, Yellow (basis for all other colors)
- **Secondary Colors**: Green, Orange, Purple (created by mixing primary colors)
- **Tertiary Colors**: Mix of primary and secondary colors
- **Color Harmonies**: Ways to combine colors for aesthetic appeal, including complementary, analogous, and triadic color schemes.

## What Are Named Colors in CSS, and When to Use Them?
CSS provides a set of predefined color names, such as `red`, `blue`, `green`, and `goldenrod`.

### When to Use Named Colors:
- For quick styling without needing specific shades
- When readability and simplicity are priorities
- When working on basic projects or prototyping

**Example:**
```css
body {
    background-color: lightblue;
    color: darkred;
}
```

## What Is the RGB Color Model, and How Does the RGB Function Work in CSS?
The RGB color model represents colors using **Red, Green, and Blue** values ranging from `0` to `255`.

### CSS `rgb()` Function:
- Defines colors using `rgb(red, green, blue)`
- Each value is between `0` (no color) and `255` (full intensity)
- Can include an alpha channel (`rgba()`) for transparency

**Example:**
```css
div {
    background-color: rgb(255, 0, 0); /* Pure Red */
    color: rgba(0, 255, 0, 0.5); /* Semi-transparent Green */
}
```

## What Is the HSL Color Model, and How Does the HSL Function Work in CSS?
The HSL model stands for **Hue, Saturation, and Lightness**:
- **Hue (H)**: The type of color, from `0` to `360` degrees (0 = Red, 120 = Green, 240 = Blue)
- **Saturation (S)**: The intensity of the color (`0%` = gray, `100%` = full color)
- **Lightness (L)**: The brightness of the color (`0%` = black, `100%` = white)

### CSS `hsl()` Function:
```css
div {
    background-color: hsl(200, 100%, 50%); /* Bright Blue */
    color: hsla(0, 100%, 50%, 0.7); /* Semi-transparent Red */
}
```

## What Are Hex Codes, and How Do They Work in CSS?
Hex codes define colors using a six-character format: `#RRGGBB`.
- Each pair (`RR`, `GG`, `BB`) represents **Red, Green, and Blue** values in hexadecimal (00-FF).
- Shortened formats like `#FFF` are also valid.

**Example:**
```css
div {
    background-color: #ff5733; /* Orange */
    color: #008080; /* Teal */
}
```

## What Are Linear and Radial Gradients, and How Do They Work in CSS?
Gradients create smooth transitions between colors in CSS.

### **Linear Gradients**:
Define a straight-line color transition.
```css
div {
    background: linear-gradient(to right, red, blue);
}
```

### **Radial Gradients**:
Define a circular color transition.
```css
div {
    background: radial-gradient(circle, yellow, green);
}
```

---
These notes cover the basics of color theory and how colors work in CSS. You can save this file on GitHub for future reference!

