# CSS Attribute Selectors Cheat Sheet

## What Is the Attribute Selector, and How Can It Be Used to Target Links with the `href` and `title` Attributes?

The **attribute selector** in CSS allows you to style elements based on their attributes. It is useful for selecting elements dynamically without adding extra classes or IDs.

### Syntax
```css
/* Selects all anchor (`<a>`) tags with an `href` attribute */
a[href] {
  color: blue;
  text-decoration: underline;
}

/* Selects all anchor tags with a specific `title` attribute */
a[title="example"] {
  color: red;
  font-weight: bold;
}
```

### Example HTML
```html
<a href="https://example.com" title="example">Visit Example</a>
<a href="https://google.com">Google</a>
```

## How to Use the Attribute Selector to Target Elements with the `lang` and `data-lang` Attributes

The `lang` and `data-lang` attributes define the language of the content. The attribute selector can be used to target specific languages.

### Syntax
```css
/* Select elements with a specific `lang` attribute */
p[lang="fr"] {
  font-style: italic;
  color: green;
}

/* Select elements where `data-lang` contains "en" */
p[data-lang*="en"] {
  border: 1px solid blue;
}
```

### Example HTML
```html
<p lang="fr">Ceci est un texte en français.</p>
<p data-lang="en-US">This is English text.</p>
```

## How to Use the Attribute Selector to Target Ordered List Elements with the `type` Attribute

The `type` attribute in an ordered list (`<ol>`) specifies the numbering style. The attribute selector can be used to target different list styles.

### Syntax
```css
/* Select ordered lists with type "A" */
ol[type="A"] {
  list-style-type: upper-alpha;
  color: purple;
}

/* Select ordered lists with type "i" (lowercase Roman numerals) */
ol[type="i"] {
  list-style-type: lower-roman;
  color: brown;
}
```

### Example HTML
```html
<ol type="A">
  <li>Item 1</li>
  <li>Item 2</li>
</ol>

<ol type="i">
  <li>First</li>
  <li>Second</li>
</ol>
```

Save this `.md` file and upload it to your GitHub repository for future reference!


