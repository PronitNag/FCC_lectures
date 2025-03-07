# Accessibility Notes

## What Is the `aria-controls` Attribute, and How Does It Work?

The `aria-controls` attribute is used to establish a relationship between an element and another element that it controls. This helps assistive technologies understand that an element (like a button) affects another part of the interface (like a dropdown menu).

### Example:
```html
<button id="menuButton" aria-controls="menu">Open Menu</button>
<ul id="menu" hidden>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

In this example, the button "controls" the menu, making it clear to assistive technologies.

---

## What Is the `aria-describedby` Attribute, and How Does It Work?

The `aria-describedby` attribute provides additional descriptive information about an element. This is useful for giving extra context to users of screen readers.

### Example:
```html
<input type="text" id="username" aria-describedby="usernameHelp">
<p id="usernameHelp">Enter a unique username with at least 8 characters.</p>
```

Here, the input field is linked to the paragraph, ensuring screen readers read the helpful description.

---

## When Is the `alt` Attribute Needed, and What Are Some Examples of Good Alt Text?

The `alt` attribute is required for images to provide textual alternatives for screen readers. It should describe the function or content of the image.

### Examples:
```html
<img src="logo.png" alt="Company Logo">
<img src="chart.png" alt="Bar chart showing quarterly sales growth.">
```

Poor alt text: `alt="image123"` (not descriptive)

Good alt text: `alt="Smiling child playing with a red ball in the park."`

---

## What Are the Accessibility Benefits for Good Link Text, and What Are Examples of Good Link Text?

Descriptive link text helps users understand the purpose of a link, especially for screen reader users who navigate by links.

### Examples:
- ❌ **Bad:** `<a href="report.pdf">Click here</a>` (Unclear purpose)
- ✅ **Good:** `<a href="report.pdf">Download the annual sales report (PDF)</a>`

---

## What Are Good Ways to Make Audio and Video Content Accessible?

1. **Provide Captions/Subtitles:** Helps users with hearing impairments.
   ```html
   <video controls>
     <source src="video.mp4" type="video/mp4">
     <track src="captions.vtt" kind="subtitles" srclang="en" label="English">
   </video>
   ```
2. **Include Transcripts:** Provide a text version of the content.
3. **Use Audio Descriptions:** Describe visual content for visually impaired users.
4. **Allow Keyboard Controls:** Ensure users can pause/play with the keyboard.

---

## What Are Some Ways to Make Web Applications Keyboard Accessible?

1. **Ensure All Interactive Elements Are Focusable:**
   ```html
   <button>Click Me</button>
   <a href="#">Link</a>
   ```
2. **Use Logical Tab Order:** Elements should follow a logical reading order.
3. **Provide Visible Focus Indicators:**
   ```css
   button:focus, a:focus {
     outline: 2px solid blue;
   }
   ```
4. **Use `role="button"` for Non-Button Elements:**
   ```html
   <div role="button" tabindex="0" onclick="alert('Clicked!')">Clickable Div</div>
   ```
5. **Implement Skip Links for Easy Navigation:**
   ```html
   <a href="#main-content" class="skip-link">Skip to main content</a>
   
