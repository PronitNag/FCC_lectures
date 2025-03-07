# JavaScript Date Object

The JavaScript `Date` object provides methods for working with dates and times. It allows you to create, manipulate, and format dates.

## Creating a Date Object

You can create a date object using the `Date` constructor in several ways:

```javascript
// Creates a date object with the current date and time
let now = new Date();
console.log(now);

// Creates a date object for a specific date (YYYY, MM, DD, HH, MM, SS, MS)
let specificDate = new Date(2023, 0, 15, 10, 30, 0); // Jan 15, 2023, 10:30 AM
console.log(specificDate);

// Creating a date from a string
let dateFromString = new Date("2023-03-25T12:00:00Z");
console.log(dateFromString);

// Creating a date using milliseconds since January 1, 1970
let dateFromMillis = new Date(1672531200000);
console.log(dateFromMillis);
```

## Common Methods of the Date Object

### Getting Date Components
```javascript
let date = new Date();
console.log(date.getFullYear());  // Get the year
console.log(date.getMonth());     // Get the month (0-11)
console.log(date.getDate());      // Get the day of the month (1-31)
console.log(date.getDay());       // Get the day of the week (0-6, where 0 is Sunday)
console.log(date.getHours());     // Get the hour (0-23)
console.log(date.getMinutes());   // Get the minutes (0-59)
console.log(date.getSeconds());   // Get the seconds (0-59)
console.log(date.getMilliseconds()); // Get milliseconds (0-999)
```

### Setting Date Components
```javascript
let date = new Date();
date.setFullYear(2025);
date.setMonth(5); // June (months are 0-based)
date.setDate(10);
date.setHours(14);
date.setMinutes(45);
date.setSeconds(30);
console.log(date);
```

---

# Different Ways to Format Dates

JavaScript provides multiple ways to format dates for display.

## 1. Using `toLocaleString()`

The `toLocaleString()` method allows formatting based on locale.
```javascript
let date = new Date();
console.log(date.toLocaleString("en-US")); // Default format
console.log(date.toLocaleString("en-GB")); // British format (DD/MM/YYYY)
console.log(date.toLocaleString("de-DE")); // German format
```

## 2. Using `toDateString()` and `toTimeString()`
```javascript
let date = new Date();
console.log(date.toDateString());  // Example: "Tue Mar 05 2024"
console.log(date.toTimeString());  // Example: "14:30:45 GMT+0530 (IST)"
```

## 3. Using `toISOString()`
```javascript
let date = new Date();
console.log(date.toISOString()); // Example: "2024-03-05T09:00:00.000Z"
```

## 4. Using `Intl.DateTimeFormat`
```javascript
let date = new Date();
let formatter = new Intl.DateTimeFormat("en-US", {
  year: "numeric",
  month: "long",
  day: "2-digit"
});
console.log(formatter.format(date)); // Example: "March 05, 2024"
```

## 5. Custom Formatting with Manual Methods
```javascript
let date = new Date();
let formattedDate = `${date.getFullYear()}-${date.getMonth() + 1}-${date.getDate()}`;
console.log(formattedDate); // Example: "2024-3-5"
```

These methods help in displaying dates in different formats as per requirements.

