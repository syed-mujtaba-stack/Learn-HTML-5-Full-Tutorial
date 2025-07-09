# Day 14: Service Workers

## Introduction to Service Workers
Service Workers are JavaScript files that run in the background, independent of web pages.

### Registering a Service Worker
```javascript
// Register service worker
if ('serviceWorker' in navigator) {
    navigator.serviceWorker.register('/service-worker.js')
        .then(registration => {
            console.log('Service Worker registered');
        })
        .catch(error => {
            console.error('Service Worker registration failed:', error);
        });
}
```

### Service Worker Lifecycle
1. Installing
2. Activating
3. Running
4. Updating

### Cache API
```javascript
// Cache assets
self.addEventListener('install', event => {
    event.waitUntil(
        caches.open('my-cache').then(cache => {
            return cache.addAll([
                '/index.html',
                '/styles.css',
                '/script.js'
            ]);
        })
    );
});

// Serve cached content
self.addEventListener('fetch', event => {
    event.respondWith(
        caches.match(event.request).then(response => {
            return response || fetch(event.request);
        })
    );
});
```

## Exercise
Create a Progressive Web App (PWA) that:
1. Registers a service worker
2. Caches assets for offline use
3. Handles push notifications
4. Syncs data in the background
5. Updates content when online

Save your work as `exercise.html` in this folder.
