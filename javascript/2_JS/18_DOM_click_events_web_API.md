# What Is an API, and What Are Web APIs?

An **API (Application Programming Interface)** is a set of rules that allows different software applications to communicate with each other. APIs define methods and data formats that programs can use to request and exchange information.

A **Web API** is an API that is accessible over the web using HTTP requests. It allows clients (such as web browsers or mobile apps) to communicate with servers to fetch or send data.

### Example:
```javascript
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data));
```
The above example makes a GET request to a web API and logs the received data.

---

# What Is the DOM, and How Do You Access Elements?

The **Document Object Model (DOM)** represents the structure of an HTML document as a hierarchical tree of objects. It allows JavaScript to dynamically access and manipulate content, structure, and styles of a webpage.

### Accessing Elements:
- **By ID:**
```javascript
let element = document.getElementById('myElement');
console.log(element.textContent);
```
- **By Class Name:**
```javascript
let elements = document.getElementsByClassName('myClass');
```
- **By Tag Name:**
```javascript
let paragraphs = document.getElementsByTagName('p');
```
- **By CSS Selector:**
```javascript
let firstItem = document.querySelector('.item');
let allItems = document.querySelectorAll('.item');
```

---

# How Do DOM Nodes Exist Relative to Each Other in the DOM Tree?

The DOM arranges elements in a **tree structure** where nodes have hierarchical relationships:
- **Parent Node**: The node above another node.
- **Child Node**: A node directly inside another node.
- **Sibling Nodes**: Nodes that share the same parent.

### Example:
```javascript
console.log(document.body.parentNode); // <html>
console.log(document.body.children);   // HTMLCollection of child elements
console.log(document.body.firstChild); // First child node
console.log(document.body.lastChild);  // Last child node
```

---

# What Is the querySelectorAll() Method, and When Should You Use It?

The `querySelectorAll()` method selects all elements that match a given CSS selector and returns a **NodeList**, which is similar to an array but lacks some array methods.

### Example:
```javascript
let items = document.querySelectorAll('.item');
items.forEach(item => console.log(item.textContent));
```
**When to use?**
- When selecting multiple elements.
- When using advanced CSS selectors.
- When `getElementsByClassName()` or `getElementsByTagName()` are insufficient.

---

# How Do You Create New Nodes Using innerHTML and createElement()?

### Using `innerHTML`:
Modifies the HTML content inside an element.
```javascript
document.body.innerHTML += '<p>New Paragraph</p>';
```
⚠️ **Security Warning**: Avoid using `innerHTML` with user input as it may cause **XSS (Cross-Site Scripting)** attacks.

### Using `createElement()`:
A safer and more flexible method.
```javascript
let newPara = document.createElement('p');
newPara.textContent = 'New Paragraph';
document.body.appendChild(newPara);
```

---

# What Is the Difference Between innerText, textContent, and innerHTML?

- **`innerText`**: Gets/sets only visible text.
- **`textContent`**: Gets/sets all text, including hidden elements.
- **`innerHTML`**: Gets/sets raw HTML content.

### Example:
```javascript
let div = document.getElementById('example');
console.log(div.innerText);    // Visible text only
console.log(div.textContent); // All text, even hidden
console.log(div.innerHTML);   // Full HTML content inside
```

---

# How Do You Add and Remove Nodes from the DOM with appendChild() and removeChild()?

### Adding Elements:
```javascript
let parent = document.getElementById('container');
let child = document.createElement('div');
child.textContent = 'New Element';
parent.appendChild(child);
```

### Removing Elements:
```javascript
parent.removeChild(child);
```

---

# How Do the Navigator, Window, and Document Work?

- **`window`**: Represents the entire browser window.
- **`document`**: Represents the web page loaded in the window.
- **`navigator`**: Provides information about the browser and system.

### Example:
```javascript
console.log(window.innerWidth); // Browser width
console.log(document.title); // Page title
console.log(navigator.userAgent); // Browser info
```

---

# How Do You Add Attributes with setAttribute()?

Sets an attribute on an element dynamically.
```javascript
let link = document.createElement('a');
link.setAttribute('href', 'https://example.com');
document.body.appendChild(link);
```

---

# What Is the Event Object?

An object that provides details about an event when it occurs.
```javascript
document.addEventListener('click', function(event) {
  console.log(event.target); // Element clicked
});
```

---

# How Does the addEventListener Method Work?

Attaches an event handler to an element.
```javascript
button.addEventListener('click', () => alert('Clicked!'));
```

---

# How Does the removeEventListener Method Work?

Removes an event handler previously attached.
```javascript
function logEvent() { console.log('Clicked!'); }
button.addEventListener('click', logEvent);
button.removeEventListener('click', logEvent);
```

---

# What Are Inline Event Handlers, and Why Is It Best Practice to Use addEventListener Instead?

**Inline handlers (Not recommended):**
```html
<button onclick="alert('Clicked!')">Click Me</button>
```
**Better approach using `addEventListener()`:**
```javascript
button.addEventListener('click', () => alert('Clicked!'));
```
✅ **Best practice:** Keeps JavaScript separate from HTML.

---

# How Do You Manipulate Styles Using Element.style and Element.classList?

### Using `style`:
```javascript
div.style.color = 'red';
```

### Using `classList`:
```javascript
div.classList.add('highlight');
```

---

# What Is the DOMContentLoaded Event, and How Does It Work?

Fires when the DOM is fully loaded.
```javascript
document.addEventListener('DOMContentLoaded', () => {
  console.log('DOM is fully loaded');
});
```

---

# How Do the setTimeout and setInterval Methods Work?

Delays execution or repeats tasks.
```javascript
setTimeout(() => console.log('Hello after 2s'), 2000);
let interval = setInterval(() => console.log('Every second'), 1000);
clearInterval(interval);
```

---

# What Is the requestAnimationFrame() API, and How Can It Be Used?

Efficiently animates elements.
```javascript
function animate() {
  console.log('Animating...');
  requestAnimationFrame(animate);
}
requestAnimationFrame(animate);
```

---

# How Do You Open and Close Dialog Elements Using JavaScript?
```javascript
let dialog = document.getElementById('myDialog');
dialog.showModal();
setTimeout(() => dialog.close(), 2000);
```

