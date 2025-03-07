# CSS Custom Properties & @property Rule

## What Are CSS Custom Properties, and How Do They Work?

CSS Custom Properties (also known as CSS variables) are user-defined values that can be reused throughout a stylesheet. They allow for better maintainability and flexibility in design.

### Syntax:
```css
:root {
    --primary-color: #3498db;
    --font-size: 16px;
}

body {
    background-color: var(--primary-color);
    font-size: var(--font-size);
}
```

### How They Work:
- Defined using `--` prefix.
- Scoped inside `:root` (global) or specific selectors (local scope).
- Accessed using `var(--property-name)`, with optional fallback: `var(--property-name, fallback-value)`.

### Example with Fallback:
```css
p {
    color: var(--text-color, black); /* Uses black if --text-color is not set */
}
```

---

## What Is the @property Rule, and How Does It Work with Fallbacks?

The `@property` rule allows defining custom properties with type constraints, initial values, and inheritance behavior. It enhances CSS variables by making them work with transitions and calculations.

### Syntax:
```css
@property --angle {
    syntax: "<angle>";
    inherits: false;
    initial-value: 0deg;
}

.box {
    --angle: 45deg;
    transform: rotate(var(--angle));
}
```

### Explanation:
- `syntax`: Specifies the type (`<color>`, `<length>`, `<number>`, etc.).
- `inherits`: Determines if the property inherits from its parent.
- `initial-value`: Provides a default value if none is set.

### Example with Transition:
```css
@property --opacity-level {
    syntax: "<number>";
    inherits: false;
    initial-value: 1;
}

.button {
    --opacity-level: 0.5;
    opacity: var(--opacity-level);
    transition: --opacity-level 0.3s ease-in-out;
}
```

### Key Benefits:
- Enables animations and transitions on custom properties.
- Provides strict typing to avoid errors.
- Allows defining fallback values more effectively.

