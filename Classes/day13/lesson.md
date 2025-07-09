# Day 13: Fetch API

## Introduction to Fetch API
The Fetch API is a modern way to make HTTP requests.

### Basic Fetch
```javascript
// GET request
fetch('https://api.example.com/data')
    .then(response => response.json())
    .then(data => {
        console.log(data);
    })
    .catch(error => {
        console.error('Error:', error);
    });

// POST request
fetch('https://api.example.com/data', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json',
    },
    body: JSON.stringify({
        name: 'John Doe',
        email: 'john@example.com'
    })
})
.then(response => response.json())
.then(data => {
    console.log('Success:', data);
})
.catch((error) => {
    console.error('Error:', error);
});
```

### Fetch Methods
- GET: Retrieve data
- POST: Send data
- PUT: Update data
- DELETE: Remove data
- HEAD: Get headers
- OPTIONS: Get options

### Advanced Features
- Request headers
- Request body
- Response headers
- Response body
- Error handling
- Timeout

## Exercise
Create an application that:
1. Makes API requests using Fetch
2. Handles different HTTP methods
3. Processes JSON responses
4. Implements error handling
5. Uses async/await syntax

Save your work as `exercise.html` in this folder.
