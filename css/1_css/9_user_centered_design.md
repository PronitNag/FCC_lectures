# User Experience Design Notes

## What Is User-Centered Design?
User-Centered Design (UCD) is an iterative design process that focuses on user needs, behaviors, and feedback.

### Key Principles:
- Understand user requirements
- Design with user feedback
- Test and iterate frequently

### Example:
```js
function getUserFeedback() {
    return prompt("What do you think about this feature?");
}
console.log(getUserFeedback());
```

---
## What Are User Requirements, User Research, and Testing?

- **User Requirements**: Features and functionalities users need.
- **User Research**: Understanding user behavior through surveys and interviews.
- **Testing**: Evaluating the design for usability.

### Example of A/B Testing:
```html
<button id="testButton">Click Me</button>
<script>
  document.getElementById("testButton").onclick = () => {
    alert("Version A clicked!");
  };
</script>
```

---
## Best Practices for Designing a Dark Mode Feature

- Use **soft contrast** (avoid pure black and white)
- Provide a toggle option
- Ensure accessibility

### Example:
```css
body.dark-mode {
    background-color: #121212;
    color: #ffffff;
}
```

---
## Best Practices for Designing Breadcrumbs

- Keep them **concise**
- Use **">" or "/"** as separators
- Show **hierarchical navigation**

### Example:
```html
<nav>
  <a href="/home">Home</a> > <a href="/category">Category</a> > Product
</nav>
```

---
## Best Practices for Designing Cards

- Use **consistent spacing and alignment**
- Prioritize **visual hierarchy**
- Ensure **responsiveness**

### Example:
```html
<div class="card">
  <img src="product.jpg" alt="Product">
  <h3>Product Name</h3>
  <p>Short description</p>
</div>
```

---
## Best Practices for Designing Infinite Scrolls

- Provide **a loading indicator**
- Offer **a way to jump to specific sections**

### Example:
```js
window.addEventListener("scroll", () => {
    if (window.innerHeight + window.scrollY >= document.body.offsetHeight) {
        loadMoreContent();
    }
});
```

---
## Best Practices for Designing Modal Dialogs

- Keep modals **simple and non-intrusive**
- Provide a **clear close button**

### Example:
```html
<div id="modal">
  <p>Are you sure?</p>
  <button onclick="closeModal()">Close</button>
</div>
```

---
## Best Practices for Progress Indication on Forms, Registration, and Setup

- Use **progress bars**
- Show **step indicators**

### Example:
```html
<progress value="50" max="100"></progress>
```

---
## Best Practices for Designing Shopping Carts

- Show **clear item details**
- Allow **easy quantity adjustments**
- Include **a checkout button**

### Example:
```html
<button onclick="addToCart()">Add to Cart</button>
```

---
## What Is Progressive Disclosure?

A technique where **information is revealed progressively** to reduce cognitive load.

### Example:
```html
<button onclick="showDetails()">More Info</button>
<div id="details" style="display: none;">Hidden information</div>
```

---
## What Is Deferred and Lazy Registration?

- **Deferred Registration**: Users can browse without signing up.
- **Lazy Registration**: Registration happens **only when necessary**.

### Example:
```js
if (!userRegistered) {
    showRegistrationForm();
}
