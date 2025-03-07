# CSS List and Link Styling Notes

## How Do You Space List Items Using `margin` or `line-height`?
To control spacing between list items, you can use `margin` or `line-height`:

```css
ul {
  list-style-type: disc; /* Default bullet points */
}

li {
  margin-bottom: 10px; /* Adds space below each list item */
  line-height: 1.5; /* Increases space between lines */
}
```

This ensures better readability and spacing between items.

---

## How Do the Different `list-style` Properties Work?
The `list-style` property in CSS allows customization of lists:

```css
ul {
  list-style-type: square; /* Changes bullet style */
  list-style-position: inside; /* Moves bullets inside content */
  list-style-image: url('bullet.png'); /* Custom bullet image */
}
```
### Breakdown:
- `list-style-type`: Defines bullet styles (`disc`, `circle`, `square`, etc.).
- `list-style-position`: Can be `inside` (aligned with text) or `outside` (default).
- `list-style-image`: Uses a custom image instead of default bullets.

---

## Why Are Default Link Styles Important for Usability on the Web?
Default link styles help users identify clickable elements. Web browsers apply these styles automatically:

```css
a {
  color: blue; /* Default color for unvisited links */
  text-decoration: underline; /* Indicates clickability */
}
```
**Usability Benefits:**
- **Consistency:** Users expect links to be underlined and colored.
- **Accessibility:** Helps visually impaired users identify links.
- **Readability:** Clear differentiation between normal text and links.

---

## How Do You Style the Different Link States?
CSS provides pseudo-classes for different link states:

```css
a:link {
  color: blue; /* Default link color */
}

a:visited {
  color: purple; /* Color for visited links */
}

a:hover {
  color: red; /* Changes color when hovered */
  text-decoration: none; /* Removes underline on hover */
}

a:active {
  color: green; /* Color when actively clicked */
}
```
### Explanation:
- `:link` → Default style for unvisited links.
- `:visited` → Style for links that have been clicked before.
- `:hover` → Style when the mouse is over the link.
- `:active` → Style when the link is clicked.

This improves user experience by providing clear visual feedback.
