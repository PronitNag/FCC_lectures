# JavaScript Event Handling Notes

## What Is the Change Event, and How Does It Work?

## What is the change event, and how does it work?

The `change` event is a special event that is fired when the user modifies the value of certain input elements. More specifically:

- When a checkbox is ticked or unticked.
- When a radio button is ticked.
- When the user makes a selection from something like a date picker or dropdown menu.
- When an input loses focus (the user tabs to the next field, or clicks out of the form) after the user has changed the value.
- When the user otherwise confirms the value, such as by hitting enter after typing some text.

> **Note:** The `change` event does **not** fire when a user types in an input. The `change` event will only fire after they have focused on another element.

The `change` event still generates an `Event` object, but unlike most other events, it does not generate a custom implementation – the only properties and methods you will have access to are those on the base `Event` object.

This differs from the `input` event, which generates a dedicated `InputEvent` object. The `change` event also differs in a few ways. An `input` event **will** trigger when a user types content into a field, for example.

These differences are important to remember, as you might get tripped up by the timing of these events firing.



The `change` event in JavaScript is triggered when the value of an input element (such as `<input>`, `<textarea>`, or `<select>`) is changed and the element loses focus.

### Example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Change Event Example</title>
    <script>
        function handleChange(event) {
            console.log("New value:", event.target.value);
        }
    </script>
</head>
<body>
    <input type="text" id="myInput" onchange="handleChange(event)">
</body>
</html>
```

### Key Points:
- The event fires when the element loses focus after a value change.
- It does **not** trigger for every keystroke (use `input` event for real-time changes).

---

## How Do Event Bubbling and Event Delegation Work?

# How do Event Bubbling and Event Delegation Work?

## Event Bubbling

Event bubbling, or propagation, refers to how an event "bubbles up" to parent objects when triggered. For example, consider this code:

```html
<p>
  <span>Click me~!</span>
</p>
```

The `<p>` element here would be considered the parent of the `<span>` element.

When you click on the `<span>` element, it becomes the target of a click event. That event, however, also bubbles up to the parent – the `<p>` element can receive and consume that event as needed.

But what does this actually mean? Well, you could attach an event listener to the `<p>` element:

```javascript
const p = document.querySelector("p");
p.addEventListener("click", (event) => {
  console.log(event.target);
});
```

Then, when you click on the `<span>` element, you will see the text `Click me~!` logged to the console.

The event propagates to the parent `<p>` element, which consumes it in an event listener to display the target of the event.

Notice how the target is still the `<span>` element. This is because the `<span>` element received the initial click.

### Expanding the Code

```javascript
const p = document.querySelector("p");
const span = document.querySelector("span");
p.addEventListener("click", (event) => {
  console.log("P listener: ");
  console.log(event.target);
});
span.addEventListener("click", (event) => {
  console.log("Span listener: ");
  console.log(event.target);
});
```

#### Console Output (Clicking on `<span>`) 
```
"Span listener: "
<span>Click me~!</span>
"P listener: "
<span>Click me~!</span>
```

### Preventing Event Propagation

Using `stopPropagation()`, we can prevent the event from bubbling up:

```javascript
const p = document.querySelector("p");
const span = document.querySelector("span");
p.addEventListener("click", (event) => {
  console.log("P listener: ");
  console.log(event.target);
});
span.addEventListener("click", (event) => {
  console.log("Span listener: ");
  console.log(event.target);
  event.stopPropagation();
});
```

#### Console Output (Clicking on `<span>`) 
```
"Span listener: "
<span>Click me~!</span>
```

This time, the `<p>` listener does not trigger because propagation was stopped in the `<span>`'s event listener.

---

## Event Delegation

Event delegation is the process of capturing an event and delegating it to another element.

Consider this update to our code, which changes the clicked `<span>` element's color to red:

```javascript
const p = document.querySelector("p");
const span = document.querySelector("span");
p.addEventListener("click", (event) => {});
span.addEventListener("click", (event) => {
  event.target.style.color = "red";
});
```

But what if there are multiple `<span>` elements, or more are created dynamically?

Instead of attaching an event listener to each `<span>`, we can delegate event handling to the `<p>` element:

```javascript
const p = document.querySelector("p");
p.addEventListener("click", (event) => {
  event.target.style.color = "red";
});
```

Now, let's generate multiple `<span>` elements:

```html
<p>
  <span>Click me~!</span>
  <span>Click me~!</span>
  <span>Click me~!</span>
  <span>Click me~!</span>
</p>
```

Clicking any `<span>` will turn it red. With a single event listener, we allow click events to bubble up and delegate handling to the `<p>` element.

---

## Conclusion

Event propagation and delegation can be complex, especially with deeply nested elements. Experimenting with the provided code will help in understanding their behavior in different scenarios.


