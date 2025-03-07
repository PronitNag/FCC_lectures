# Forms, Labels, and Inputs in HTML

HTML forms are used to collect user input. A form consists of various elements like input fields, labels, buttons, etc.

### Example:
```html
<form action="submit.php" method="post">
  <label for="username">Username:</label>
  <input type="text" id="username" name="username" required>
  <button type="submit">Submit</button>
</form>
```
- `<form>`: Defines the form.
- `<label>`: Associates a text label with an input field.
- `<input>`: Used for user input.
- `required`: Ensures the field must be filled before submission.

---

# Different Types of Buttons in HTML

HTML provides different types of buttons for various actions.

### Types of Buttons:
1. **Submit Button**: Submits the form data.
   ```html
   <button type="submit">Submit</button>
   ```
2. **Reset Button**: Clears all form fields.
   ```html
   <button type="reset">Reset</button>
   ```
3. **Button Element**: Triggers JavaScript actions.
   ```html
   <button type="button" onclick="alert('Clicked!')">Click Me</button>
   ```

Use buttons wisely:
- **Submit** for form submission.
- **Reset** when clearing data is needed.
- **Button** for JavaScript interactions.

---

# Client-Side Form Validation in HTML

Client-side validation ensures that users enter the correct data format before submission, reducing server load.

### Examples:
1. **Required Field**
   ```html
   <input type="text" required>
   ```
2. **Pattern Matching**
   ```html
   <input type="text" pattern="[A-Za-z]{3,}" title="Enter at least 3 letters">
   ```
3. **Email Validation**
   ```html
   <input type="email" required>
   ```

These help in preventing incorrect data entry before reaching the server.

---

# Different Form States in HTML

Form elements have different states to provide better user interaction.

### Common Form States:
1. **Enabled (Default State)**
   ```html
   <input type="text">
   ```
2. **Disabled (Cannot be interacted with)**
   ```html
   <input type="text" disabled>
   ```
3. **Readonly (Visible but not editable)**
   ```html
   <input type="text" value="Fixed Value" readonly>
   ```
4. **Focused (When clicked or tabbed into)**
   ```html
   <input type="text" autofocus>
   ```
5. **Invalid (When the input does not match validation rules)**
   ```html
   <input type="email" required>
   ```
   If the email is incorrect, the browser highlights the field.

Form states improve accessibility and usability.

