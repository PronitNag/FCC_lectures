# Accessibility Tips

## 1. Tools to Check for Good Color Contrast

Color contrast is important for accessibility, ensuring text is readable by users with visual impairments. Here are some tools to check for good contrast:

### Online Tools
- **WebAIM Contrast Checker** ([webaim.org](https://webaim.org/resources/contrastchecker/))
- **Contrast Ratio by Lea Verou** ([contrast-ratio.com](https://contrast-ratio.com/))
- **Accessible Colors** ([accessible-colors.com](https://accessible-colors.com/))

### Browser Extensions
- **WAVE (Web Accessibility Evaluation Tool)**
- **axe DevTools by Deque**
- **Color Contrast Analyzer (CCA) by TPGi**

### DevTools
- Chrome DevTools: 
  - Open **DevTools** → **Elements tab**
  - Select an element → Check **Accessibility (A11y) properties**
  - Contrast ratio is displayed automatically

### CSS Example for Good Contrast
```css
body {
  background-color: #ffffff; /* Light background */
  color: #222222; /* Dark text for better readability */
}
```

---

## 2. Best Practices for Hiding Content Without Making It Inaccessible

Sometimes, content needs to be hidden from sighted users but should still be accessible to screen readers.

### Recommended Methods
#### 1. **Use `aria-hidden` for Decorative Content**
```html
<span aria-hidden="true">★</span> 5-star rating
```
- `aria-hidden="true"` hides the element from screen readers.

#### 2. **Use CSS to Visually Hide While Keeping Content Accessible**
```css
.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
```
```html
<p class="visually-hidden">This content is only for screen readers</p>
```

#### 3. **Use `display: none` or `visibility: hidden` When Completely Hiding Content**
```css
.hidden {
  display: none;
}
```
```html
<p class="hidden">This content is completely hidden</p>
```
- ⚠️ **Note:** This method hides content from both sighted users and screen readers.

### Summary
| Method | Visible to Sighted Users? | Readable by Screen Readers? |
|--------|----------------|-----------------|
| `aria-hidden="true"` | ✅ Yes | ❌ No |
| `.visually-hidden` CSS | ❌ No | ✅ Yes |
| `display: none` | ❌ No | ❌ No |

Using the correct method depends on whether the content should be available to assistive technologies.

