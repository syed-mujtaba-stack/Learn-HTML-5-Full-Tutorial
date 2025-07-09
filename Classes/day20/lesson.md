# Day 20: Progressive Web Apps (PWA) Essentials

## Overview
Progressive Web Apps (PWAs) combine the best of web and mobile apps. They work offline, can be installed on devices, and provide a native-like experience using standard web technologies.

---

## 1. Web App Manifest
A `manifest.json` file describes your app to the browser:
- `name`, `short_name`: App names
- `start_url`: Where the app should start
- `display`: Standalone or fullscreen
- `theme_color`, `background_color`: UI colors
- `icons`: App icons for homescreen/install

**Example:**
```json
{
  "name": "HTML5 PWA Demo",
  "short_name": "HTML5PWA",
  "start_url": ".",
  "display": "standalone",
  "background_color": "#ffffff",
  "theme_color": "#2196f3",
  "icons": [
    { "src": "icon-192.png", "sizes": "192x192", "type": "image/png" },
    { "src": "icon-512.png", "sizes": "512x512", "type": "image/png" }
  ]
}
```

---

## 2. Service Worker
A service worker is a background script that can cache files, handle network requests, and enable offline support.

**Registration:**
```js
if ('serviceWorker' in navigator) {
  navigator.serviceWorker.register('sw.js');
}
```

**Basic Service Worker:**
```js
const CACHE_NAME = 'pwa-demo-cache-v1';
const ASSETS = [
  '/',
  'index.html',
  'manifest.json',
  'icon-192.png',
  'icon-512.png',
];
self.addEventListener('install', event => {
  event.waitUntil(
    caches.open(CACHE_NAME).then(cache => cache.addAll(ASSETS))
  );
});
self.addEventListener('fetch', event => {
  event.respondWith(
    caches.match(event.request).then(response => response || fetch(event.request))
  );
});
```

---

## 3. Add to Home Screen
With a valid manifest and service worker, browsers will prompt users to install the app. This works on mobile and desktop (Chrome/Edge).

---

## 4. Testing PWA Features
- **Offline:** Disconnect from the network and reload the app.
- **Install:** Look for "Add to Home Screen" or install prompt in browser menu.
- **DevTools:** Use the Application panel to check manifest and service worker status.

---

## Best Practices
- Use HTTPS for all PWA features.
- Provide icons in multiple sizes.
- Keep your service worker up to date.
- Test installability and offline support regularly.

## Resources
- [MDN: Progressive web apps (PWAs)](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps)
- [Google Web Fundamentals: PWA](https://web.dev/progressive-web-apps/)
- [Web App Manifest Generator](https://app-manifest.firebaseapp.com/)

---

**Congratulations!** You've completed the 20-day HTML5 advanced tutorial series. Try the exercise and solution files to make your own site installable and offline-ready!
