# JavaScript Event Handling Notes

## What Is the Change Event, and How Does It Work?

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

### Event Bubbling:
Event bubbling is a propagation method where an event starts at the target element and moves up through its ancestors (parent, grandparent, etc.).

### Example:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Event Bubbling Example</title>
    <script>
        document.getElementById("child").addEventListener("click", function() {
            alert("Child Clicked");
        });

        document.getElementById("parent").addEventListener("click", function() {
            alert("Parent Clicked");
        });
    </script>
</head>
<body>
    <div id="parent" style="padding: 20px; background: lightgray;">
        Parent
        <button id="child">Click Me</button>
    </div>
</body>
</html>
```
### Key Points:
- Clicking the `button` triggers both its own event and the parent `<div>` event due to bubbling.
- The event flows upwards from child to parent.

### Event Delegation:
Instead of attaching an event listener to multiple child elements, you can use event delegation by adding a listener to a common ancestor and handling events based on the target.

### Example:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Event Delegation Example</title>
    <script>
        document.getElementById("list").addEventListener("click", function(event) {
            if (event.target.tagName === "LI") {
                alert("You clicked on: " + event.target.textContent);
            }
        });
    </script>
</head>
<body>
    <ul id="list">
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>
</body>
</html>
```

### Key Points:
- The event is captured at the parent (`ul`) and handled based on the clicked child (`li`).
- More efficient than adding individual listeners to each child element.

---

