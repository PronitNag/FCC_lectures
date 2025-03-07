# CSS Pseudo-classes and Pseudo-elements

## What Are Pseudo-classes, and How Do They Work?
Pseudo-classes define a special state of an element. They allow styling elements based on user interactions, element positions, or states without needing extra classes or JavaScript.

### Example:
```css
/* Style links only when hovered */
a:hover {
    color: red;
}
```

## Examples of Element User Action Pseudo-classes
These pseudo-classes apply styles based on user actions.

### Examples:
```css
/* Change background color when hovering over a button */
button:hover {
    background-color: yellow;
}

/* Apply styles when a button is being clicked */
button:active {
    transform: scale(0.95);
}
```

## Examples of Input Pseudo-classes
These pseudo-classes apply styles based on input field states.

### Examples:
```css
/* Style an input when it is focused */
input:focus {
    border: 2px solid blue;
}

/* Style a required input field */
input:required {
    border: 1px solid red;
}
```

## Examples of Location Pseudo-classes
These pseudo-classes apply styles based on the hyperlink's state.

### Examples:
```css
/* Style visited links */
a:visited {
    color: purple;
}

/* Style links that are currently active (being clicked) */
a:active {
    color: green;
}
```

## Examples of Tree-structural Pseudo-classes
These pseudo-classes style elements based on their position in the DOM tree.

### Examples:
```css
/* Style the first child of a container */
div:first-child {
    font-weight: bold;
}

/* Style every even row in a table */
tr:nth-child(even) {
    background-color: lightgray;
}
```

## Examples of Functional Pseudo-classes
Functional pseudo-classes take arguments to target elements dynamically.

### Examples:
```css
/* Select the third child of a container */
div:nth-child(3) {
    color: blue;
}

/* Select the last child of a container */
div:last-child {
    text-decoration: underline;
}
```

## What Are Pseudo-elements, and How Do They Work?
Pseudo-elements allow styling specific parts of an element.

### Examples:
```css
/* Style the first letter of a paragraph */
p::first-letter {
    font-size: 2em;
    color: red;
}

/* Add content before an element */
p::before {
    content: "Note: ";
    font-weight: bold;
    color: green;
}

