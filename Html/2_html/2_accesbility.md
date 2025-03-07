# Accessibility and ARIA Notes

## Why Is It Important for Inputs to Have an Associated Label?
Labels provide context to input fields, making them accessible to screen readers and improving usability.

### Example:
```html
<label for="username">Username:</label>
<input type="text" id="username" name="username">
```

---

## What Is the Purpose of WAI-ARIA, and How Does It Work?
WAI-ARIA (Web Accessibility Initiative – Accessible Rich Internet Applications) improves the accessibility of web content, especially dynamic content and complex UIs.

### Example:
```html
<button aria-disabled="true">Submit</button>
```

---

## What Are ARIA Roles?
ARIA roles define the purpose of an element to assistive technologies.

### Example:
```html
<div role="alert">This is an important alert!</div>
```

---

## What Are the Roles of the `aria-label` and `aria-labelledby` Attributes?
- `aria-label`: Provides an accessible name.
- `aria-labelledby`: References another element for labeling.

### Example:
```html
<button aria-label="Close">X</button>
<p id="desc">This button submits the form</p>
<button aria-labelledby="desc">Submit</button>
```

---

## What Is the `aria-hidden` Attribute, and How Does It Work?
Hides an element from assistive technologies without removing it from the DOM.

### Example:
```html
<p aria-hidden="true">This text will be ignored by screen readers.</p>
```

---

## What Is the `aria-expanded` Attribute, and How Does It Work?
Indicates the expanded or collapsed state of an element.

### Example:
```html
<button aria-expanded="false" onclick="toggleMenu()">Menu</button>
```

---

## What Is the `aria-live` Attribute, and How Does It Work?
Announces dynamic content updates to screen readers.

### Example:
```html
<div aria-live="polite">Updating content...</div>
```

---

## What Are Some Common ARIA States Used on Custom Control Elements?
- `aria-checked` (for checkboxes)
- `aria-disabled` (for disabled elements)
- `aria-selected` (for selected items)

### Example:
```html
<input type="checkbox" aria-checked="false"> Accept Terms

