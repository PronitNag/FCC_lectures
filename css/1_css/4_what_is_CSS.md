# CSS Basics Notes

## What Is CSS, and What Is Its Role on the Web?
CSS (Cascading Style Sheets) is a stylesheet language used to describe the presentation of a document written in HTML. It controls the layout, colors, fonts, and responsiveness of web pages.

Example:
```css
body {
    background-color: lightblue;
    font-family: Arial, sans-serif;
}
```

## What Is the Basic Anatomy of a CSS Rule?
A CSS rule consists of a selector, a property, and a value.

Example:
```css
p {
    color: red;  /* property: value */
    font-size: 16px;
}
```

## What Is the Meta Viewport Element Used For?
The `<meta>` viewport element controls how web pages are displayed on mobile devices.

Example:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
This ensures the page scales correctly on different devices.

## What Are Some Default Browser Styles Applied to HTML?
Browsers apply default styles known as "User-Agent Styles." For example, `<h1>` tags are bold and larger, and `<p>` tags have margins.

Example:
```css
h1 {
    font-size: 2em; /* Default style */
}
```

## What Are Inline, Internal, and External CSS, and When Should You Use Each One?
- **Inline CSS**: Applied directly within an element.
  ```html
  <p style="color: blue;">This is inline CSS</p>
  ```
  *Use for quick styling or overriding styles.*

- **Internal CSS**: Defined in a `<style>` tag within HTML.
  ```html
  <style>
      p { color: green; }
  </style>
  ```
  *Use for small projects or specific pages.*

- **External CSS**: Linked via an external file.
  ```html
  <link rel="stylesheet" href="styles.css">
  ```
  *Use for large projects and maintainability.*

## How Do Width and Height Work?
The `width` and `height` properties define an element's dimensions. 

Example:
```css
div {
    width: 200px;
    height: 100px;
}
```
Use `max-width`, `min-height`, etc., for flexible layouts.

## What Are the Different Types of CSS Combinators?
CSS combinators define relationships between selectors:

- **Descendant (` `)**
  ```css
  div p { color: red; }
  ```
- **Child (`>`)**
  ```css
  div > p { color: blue; }
  ```
- **Adjacent Sibling (`+`)**
  ```css
  h1 + p { color: green; }
  ```
- **General Sibling (`~`)**
  ```css
  h1 ~ p { color: purple; }
  ```

## What Is the Difference Between Inline and Block-Level Elements in CSS?
- **Block Elements**: Take up full width (e.g., `<div>`, `<p>`, `<h1>`).
- **Inline Elements**: Only take up as much width as needed (e.g., `<span>`, `<a>`).

Example:
```css
div { display: block; }
span { display: inline; }
```

## How Does Inline-Block Work, and How Does It Differ from Inline and Block Elements?
`inline-block` behaves like `inline`, but allows width and height settings.

Example:
```css
div {
    display: inline-block;
    width: 100px;
    height: 50px;
}
```

## What Are Margins and Padding, and How Do They Work?
- **Margin**: Space outside an element.
- **Padding**: Space inside an element, between content and border.

Example:
```css
div {
    margin: 10px;
    padding: 20px;
}

