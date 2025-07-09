# Day 11: Web Workers

## What are Web Workers?
Web Workers allow you to run JavaScript in background threads.

### Creating a Worker
```javascript
// Create worker
const worker = new Worker('worker.js');

// Send message to worker
worker.postMessage({data: 'Hello'});

// Receive message from worker
worker.onmessage = function(event) {
    console.log('Received: ' + event.data);
};

// Terminate worker
worker.terminate();
```

### Worker Script (worker.js)
```javascript
// Listen for messages
self.onmessage = function(event) {
    // Process data
    const result = process(event.data);
    
    // Send result back
    self.postMessage(result);
};

// Error handling
self.onerror = function(error) {
    console.error('Worker error: ' + error.message);
};
```

### Worker Types
- Dedicated Workers: For single use
- Shared Workers: Can be shared between multiple scripts
- Service Workers: For background tasks and push notifications

## Exercise
Create an application that demonstrates:
1. Background processing using Web Workers
2. Communication between main thread and worker
3. Error handling
4. Progress updates
5. Multiple worker instances

Save your work as `exercise.html` in this folder.
