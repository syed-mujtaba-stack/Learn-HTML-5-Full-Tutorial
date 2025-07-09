# Day 8: Web Storage

## HTML5 Web Storage
Web Storage provides ways to store data locally within the user's browser.

### localStorage
- Persists even after the browser is closed
- No expiration time
- Limited to 5-10MB
- Syntax:
```javascript
// Store data
localStorage.setItem('key', 'value');

// Retrieve data
let value = localStorage.getItem('key');

// Remove data
localStorage.removeItem('key');

// Clear all data
localStorage.clear();
```

### sessionStorage
- Data is cleared when the page session ends
- Same origin policy applies
- Syntax:
```javascript
// Store data
sessionStorage.setItem('key', 'value');

// Retrieve data
let value = sessionStorage.getItem('key');
```

### IndexedDB
- More powerful than localStorage
- Can store complex data types
- Supports transactions
- Syntax:
```javascript
// Open database
const request = indexedDB.open('myDatabase', 1);

request.onsuccess = function(event) {
    const db = event.target.result;
};

request.onerror = function(event) {
    console.error('Database error: ' + event.target.errorCode);
};
```

## Exercise
Create a web application that demonstrates:
1. Storing user preferences using localStorage
2. Saving form data using sessionStorage
3. Creating a simple database using IndexedDB
4. Implementing error handling
5. Creating a UI to manage stored data

Save your work as `exercise.html` in this folder.
