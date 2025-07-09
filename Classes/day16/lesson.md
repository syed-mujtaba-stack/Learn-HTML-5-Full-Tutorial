# Day 16: IndexedDB & Client-Side Databases

## Overview
IndexedDB is a low-level API for client-side storage of significant amounts of structured data, including files/blobs. It allows you to build offline-capable, high-performance web applications that require persistent storage beyond the capabilities of localStorage or sessionStorage.

## Why IndexedDB?
- **Large Storage**: Store far more data than localStorage (which is limited to ~5MB).
- **Structured Data**: Store JavaScript objects, not just strings.
- **Asynchronous**: Non-blocking API for smooth UX.
- **Indexed**: Fast queries using indexes.
- **Transactions**: Atomic operations for reliability.

## Key Concepts
- **Database**: Each origin can have multiple named databases.
- **Object Store**: Like a table in SQL, stores records (objects) with a key.
- **Transaction**: All read/write operations happen in a transaction.
- **Cursor**: Iterate over records in the store.

## CRUD Operations Example

### 1. Opening a Database
```js
const request = indexedDB.open('notesDB', 1);
request.onupgradeneeded = function(e) {
  const db = e.target.result;
  if (!db.objectStoreNames.contains('notes')) {
    db.createObjectStore('notes', { keyPath: 'id', autoIncrement: true });
  }
};
request.onsuccess = function(e) {
  const db = e.target.result;
  // Ready to use
};
```

### 2. Adding a Record
```js
const tx = db.transaction(['notes'], 'readwrite');
const store = tx.objectStore('notes');
store.add({ title: 'My Note', content: 'Hello IndexedDB!' });
```

### 3. Reading Records
```js
const tx = db.transaction(['notes'], 'readonly');
const store = tx.objectStore('notes');
const request = store.openCursor();
request.onsuccess = function(e) {
  const cursor = e.target.result;
  if (cursor) {
    console.log(cursor.value);
    cursor.continue();
  }
};
```

### 4. Updating a Record
```js
store.put({ id: 1, title: 'Updated', content: 'Updated content' });
```

### 5. Deleting a Record
```js
store.delete(1);
```

## Practical Example: Note-Taking App
- **Add Note**: Enter a title and content, save to IndexedDB.
- **List Notes**: Display all notes from the database.
- **Edit Note**: Update title/content and save changes.
- **Delete Note**: Remove a note from the database.

## Best Practices
- Always handle errors (`onerror` handlers).
- Use transactions for atomicity.
- Clean up resources (close database if needed).
- Use feature detection: `if ('indexedDB' in window) { ... }`

## Resources
- [MDN IndexedDB Guide](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API)
- [HTML5 Rocks: Simple Todo List with IndexedDB](https://www.html5rocks.com/en/tutorials/indexeddb/todo/)

---

**Next:** Try the exercise and solution files for a hands-on experience building a persistent note-taking app with IndexedDB!
