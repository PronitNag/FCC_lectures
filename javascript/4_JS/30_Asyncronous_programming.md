# Asynchronous vs Synchronous JavaScript

## Synchronous JavaScript
- Executes code line by line.
- Each operation waits for the previous one to complete.
- Example:
  
  ```js
  console.log("Start");
  for (let i = 0; i < 5; i++) {
      console.log(i);
  }
  console.log("End");
  ```

## Asynchronous JavaScript
- Executes non-blocking operations using callbacks, promises, or async/await.
- Example:

  ```js
  console.log("Start");
  setTimeout(() => {
      console.log("Inside setTimeout");
  }, 2000);
  console.log("End");
  ```

---

# Async vs Defer Attributes in `<script>`

## `async`
- Loads script asynchronously and executes immediately when downloaded.
- Example:
  ```html
  <script async src="script.js"></script>
  ```

## `defer`
- Loads script asynchronously but waits for HTML parsing to complete before execution.
- Example:
  ```html
  <script defer src="script.js"></script>
  ```

---

# Fetch API

## Overview
- Provides a modern way to make network requests.
- Commonly used to fetch JSON, images, and other resources.

## Example:
  ```js
  fetch("https://jsonplaceholder.typicode.com/posts")
      .then(response => response.json())
      .then(data => console.log(data))
      .catch(error => console.error("Error:", error));
  ```

---

# Fetch API with HTTP Methods

## GET Request:
  ```js
  fetch("https://api.example.com/data")
      .then(res => res.json())
      .then(data => console.log(data));
  ```

## POST Request:
  ```js
  fetch("https://api.example.com/data", {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify({ name: "John" })
  })
  .then(res => res.json())
  .then(data => console.log(data));
  ```

---

# Promises and Promise Chaining

## Promise Example:
  ```js
  let promise = new Promise((resolve, reject) => {
      setTimeout(() => resolve("Done!"), 2000);
  });
  
  promise.then(result => console.log(result));
  ```

## Promise Chaining:
  ```js
  fetch("https://jsonplaceholder.typicode.com/users")
      .then(response => response.json())
      .then(users => users[0])
      .then(user => console.log(user.name))
      .catch(error => console.error(error));
  ```

---

# Async/Await

## Example:
  ```js
  async function fetchData() {
      try {
          let response = await fetch("https://jsonplaceholder.typicode.com/posts");
          let data = await response.json();
          console.log(data);
      } catch (error) {
          console.error("Error fetching data:", error);
      }
  }
  fetchData();
  ```

---

# JavaScript Engine and Runtime

## JavaScript Engine:
- Converts JavaScript code into machine code.
- Examples: V8 (Chrome, Node.js), SpiderMonkey (Firefox).

## JavaScript Runtime:
- Includes the engine, Web APIs (DOM, Fetch, setTimeout), and an event loop.
- Enables asynchronous operations.

---

# Geolocation API

## `getCurrentPosition` Example:
  ```js
  navigator.geolocation.getCurrentPosition(
      position => console.log(position.coords),
      error => console.error(error)
  );
  ```

- Fetches latitude and longitude of user's location.
- Requires user permission.

