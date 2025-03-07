# CSS Specificity and Related Concepts

## What Is CSS Specificity?
CSS specificity determines which style rule is applied when multiple rules target the same element. The specificity is calculated based on the type of selectors used.

### Specificity for Different CSS Types:
- **Inline CSS** (highest specificity): `style="color: red;"` → Specificity: `1000`
- **Internal CSS** (inside `<style>` tag): `#id {}` → Specificity: `100`
- **External CSS** (linked CSS file): `p.class {}` → Specificity: `10`

Example:
```html
<!DOCTYPE html>
<html>
<head>
    <style>
        p { color: blue; } /* Specificity: 1 */
        .text { color: green; } /* Specificity: 10 */
        #unique { color: red; } /* Specificity: 100 */
    </style>
</head>
<body>
    <p id="unique" class="text">Hello, CSS Specificity!</p>
</body>
</html>
```

---

## What Is the Universal Selector, and What Is Its Specificity?
The universal selector (`*`) applies styles to all elements but has a specificity of `0`.

Example:
```css
* {
    margin: 0;
    padding: 0;
}
```
Specificity: `0` (overridden by any other selector).

---

## What Is the Specificity for Type Selectors?
Type selectors (element selectors) apply styles to specific HTML tags and have a specificity of `1`.

Example:
```css
h1 {
    color: blue;
}
```
Specificity: `1`

---

## What Is the Specificity for Class Selectors?
Class selectors have a specificity of `10`.

Example:
```css
.warning {
    color: orange;
}
```
Specificity: `10`

---

## What Is the Specificity for ID Selectors?
ID selectors have a specificity of `100`.

Example:
```css
#main {
    color: red;
}
```
Specificity: `100`

---

## What Is the `!important` Keyword?
The `!important` rule overrides all specificity rules and applies the style forcefully.

Example:
```css
p {
    color: blue !important;
}
```
### Best Practices:
- Use `!important` sparingly.
- Avoid it in large projects.
- Prefer increasing specificity instead.

---

## How Does the Cascade Algorithm Work at a High Level?
CSS follows a **cascade** mechanism:
1. **Source Order**: Last declared style wins if selectors have equal specificity.
2. **Specificity**: Higher specificity wins.
3. **Importance**: `!important` overrides all normal rules.

---

## How Does Inheritance Work with CSS at a High Level?
Some CSS properties are **inherited**, meaning child elements receive styles from their parents.

### Inherited Properties:
- `color`
- `font-family`
- `visibility`

### Non-Inherited Properties:
- `margin`
- `padding`
- `border`

To enforce inheritance:
```css
p {
    color: inherit;
}
```
This makes `<p>` inherit the `color` from its parent.

---

These notes should help you understand CSS specificity and related topics!
