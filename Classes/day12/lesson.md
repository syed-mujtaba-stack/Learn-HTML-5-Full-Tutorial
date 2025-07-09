# Day 12: Web Components

## Introduction to Web Components
Web Components allow you to create reusable custom elements with their own functionality.

### Custom Elements
```javascript
// Define custom element
class MyElement extends HTMLElement {
    constructor() {
        super();
        this.attachShadow({ mode: 'open' });
        this.shadowRoot.innerHTML = `
            <style>
                /* Component styles */
            </style>
            <div>Custom Element Content</div>
        `;
    }
}

// Register element
customElements.define('my-element', MyElement);
```

### Shadow DOM
- Creates an isolated DOM tree
- Prevents style conflicts
- Maintains encapsulation

### HTML Templates
```html
<template id="my-template">
    <style>
        /* Component styles */
    </style>
    <div>Template Content</div>
</template>
```

## Exercise
Create a web component that:
1. Has its own template and styles
2. Accepts custom properties
3. Emits custom events
4. Handles user interactions
5. Is reusable across different pages

Save your work as `exercise.html` in this folder.
