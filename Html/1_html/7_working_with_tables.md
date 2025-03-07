# HTML Tables: Usage and Best Practices

## What Are HTML Tables Used For?
HTML tables are primarily used for displaying tabular data, where information is structured into rows and columns.

### Common Uses:
1. **Data Representation**: Presenting structured data like financial reports, schedules, or statistical information.
2. **Forms and Layouts** (with proper accessibility considerations).
3. **Comparison Charts**: Side-by-side comparisons of products or features.
4. **Invoice or Order Summary**: Organizing bills, receipts, or order details.

### Basic Table Structure:
```html
<table border="1">
    <tr>
        <th>Name</th>
        <th>Age</th>
        <th>City</th>
    </tr>
    <tr>
        <td>Amit</td>
        <td>25</td>
        <td>Mumbai</td>
    </tr>
    <tr>
        <td>Sara</td>
        <td>30</td>
        <td>Delhi</td>
    </tr>
</table>
```

## What Should HTML Tables Not Be Used For?
While tables are useful for displaying data, they should not be misused for layout purposes. In modern web design, **CSS Flexbox** and **CSS Grid** are the preferred methods for creating layouts.

### Why Avoid Using Tables for Layout?
1. **Accessibility Issues**: Screen readers may misinterpret tables used for layout.
2. **Complexity**: Making a table-based layout responsive is challenging.
3. **SEO Impact**: Search engines may not properly index table-based layouts.
4. **Maintainability**: Updating a table-based layout is difficult compared to using CSS.

### Alternative for Layout:
Instead of using tables, consider using **CSS Flexbox**:
```html
<div style="display: flex; justify-content: space-around;">
    <div>Column 1</div>
    <div>Column 2</div>
    <div>Column 3</div>
</div>
```
Or **CSS Grid**:
```html
<div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px;">
    <div>Column 1</div>
    <div>Column 2</div>
    <div>Column 3</div>
</div>
```

## Conclusion
- **Use tables for tabular data only.**
- **Avoid using tables for webpage layouts.**
- **Prefer CSS Flexbox or Grid for modern web designs.**
