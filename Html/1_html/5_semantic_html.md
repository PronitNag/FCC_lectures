# Semantic HTML and Structural Hierarchy

## Why Should You Care About Semantic HTML?
Semantic HTML improves accessibility, SEO, and maintainability by using meaningful tags.
```html
<!-- Semantic -->
<article>
  <h2>Article Title</h2>
  <p>Article content...</p>
</article>
<!-- Non-semantic -->
<div class="article">
  <h2>Article Title</h2>
  <p>Article content...</p>
</div>
```

## Why is it Important to Have Good Structural Hierarchy?
A well-structured HTML document enhances readability and accessibility.
```html
<header>
  <h1>Site Title</h1>
</header>
<main>
  <section>
    <h2>Section Title</h2>
    <p>Content...</p>
  </section>
</main>
<footer>
  <p>© 2024 Company</p>
</footer>
```

## What Is the Difference Between Presentational and Semantic HTML?
Presentational HTML defines appearance, while semantic HTML defines meaning.
```html
<!-- Presentational -->
<div style="font-weight: bold;">Important Text</div>
<!-- Semantic -->
<strong>Important Text</strong>
```

## When Should You Use the Emphasis Element Over the Idiomatic Text Element?
Use `<em>` for emphasis and `<i>` for idiomatic content like foreign words.
```html
<p>This is <em>very</em> important.</p>
<p>She said <i>bonjour</i> to greet us.</p>
```

## When Should You Use the Strong Element Over the Bring Attention To Element?
Use `<strong>` for strong importance and `<b>` for stylistic bold text.
```html
<p><strong>Warning:</strong> This action is irreversible.</p>
<p><b>Note:</b> This is just a reminder.</p>
```

## What Are Description Lists, and When Should You Use Them?
Description lists `<dl>` are used for terms and descriptions.
```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>
</dl>
```

## How Do Block and Inline Quotes Work in HTML?
Use `<blockquote>` for block quotes and `<q>` for inline quotes.
```html
<blockquote>
  <p>"The journey of a thousand miles begins with one step."</p>
</blockquote>
<p>Lao Tzu once said, <q>The journey of a thousand miles begins with one step.</q></p>
```

## How Do You Display Abbreviations and Acronyms in HTML?
Use `<abbr>` with a title attribute.
```html
<p>The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.</p>
```

## How Do You Display Addresses in HTML?
Use `<address>` for contact details.
```html
<address>
  123 Main Street, City, Country<br>
  Email: contact@example.com
</address>
```

## How Do You Display Times and Dates in HTML?
Use `<time>` for better machine readability.
```html
<p>Published on <time datetime="2024-03-06">March 6, 2024</time>.</p>
```

## How Do You Display Mathematical Equations and Chemical Formulas in HTML?
Use `<sup>` for superscripts and `<sub>` for subscripts.
```html
<p>H<sub>2</sub>O (Water)</p>
<p>E = mc<sup>2</sup></p>
```

## How Do You Represent Computer Code in HTML?
Use `<code>`, `<pre>`, and `<samp>` for different code representations.
```html
<pre><code>console.log("Hello, World!");</code></pre>
<p>Output: <samp>Hello, World!</samp></p>
```

## What Are the U, S, and Ruby Elements Used For, and How Do They Work?
- `<u>`: Underline text.
- `<s>`: Strike-through text.
- `<ruby>`: Annotate East Asian text.
```html
<p><u>Underlined text</u></p>
<p><s>Strikethrough text</s></p>
<ruby>
  漢 <rt>Kan</rt>
  字 <rt>Ji</rt>
</ruby>

