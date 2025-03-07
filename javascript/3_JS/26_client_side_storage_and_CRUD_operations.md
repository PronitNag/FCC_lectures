# CRUD Operations

CRUD stands for **Create, Read, Update, Delete**. These are the basic operations for persistent storage.

### Example using JavaScript (LocalStorage)
```javascript
// Create
localStorage.setItem("username", "JohnDoe");

// Read
console.log(localStorage.getItem("username"));

// Update
localStorage.setItem("username", "JaneDoe");

// Delete
localStorage.removeItem("username");
```

---

# localStorage

`localStorage` is a web storage API that allows storing key-value pairs persistently in a browser.

### Common Methods
```javascript
localStorage.setItem("key", "value"); // Store data
localStorage.getItem("key"); // Retrieve data
localStorage.removeItem("key"); // Remove data
localStorage.clear(); // Clear all data
```

---

# sessionStorage

Similar to `localStorage`, but data is cleared when the session ends (browser/tab is closed).

### Common Methods
```javascript
sessionStorage.setItem("sessionKey", "sessionValue");
sessionStorage.getItem("sessionKey");
sessionStorage.removeItem("sessionKey");
sessionStorage.clear();
```

---

# Cookies

Cookies store small data pieces that persist across sessions and can be sent to the server.

### Example
```javascript
document.cookie = "user=JohnDoe; expires=Fri, 31 Dec 2025 12:00:00 UTC; path=/";
console.log(document.cookie); // Read cookies
```

---

# Cache API

Used for storing network responses and assets for offline access.

### Example
```javascript
caches.open("my-cache").then(cache => {
  cache.add("/index.html");
});
```

---

# Negative Patterns in Client-Side Storage

- **Security Risks**: Data is accessible to scripts, making it vulnerable to XSS attacks.
- **Storage Limitations**: Limited size compared to databases.
- **Lack of Encryption**: Most client-side storage is not encrypted by default.

---

# Using Cookies for Arbitrary Data Storage

Cookies can store session identifiers or JSON data (base64 encoded to prevent corruption).

### Example
```javascript
const data = { user: "JohnDoe", role: "admin" };
document.cookie = `session=${btoa(JSON.stringify(data))}; path=/`;
```

---

# IndexedDB

A low-level NoSQL database for structured storage in browsers.

### Example
```javascript
let request = indexedDB.open("myDatabase", 1);
request.onsuccess = function(event) {
  let db = event.target.result;
  console.log("Database opened successfully");
};
```

---

# Cache & Service Workers

**Service Workers** intercept network requests and serve cached responses for offline functionality.

### Example
```javascript
self.addEventListener("install", event => {
  event.waitUntil(
    caches.open("v1").then(cache => {
      return cache.addAll(["/index.html", "/styles.css"]);
    })
  );
});

