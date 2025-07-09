# Day 10: Drag and Drop API

## HTML5 Drag and Drop
HTML5 provides native drag and drop functionality.

### Basic Drag and Drop
```html
<!-- Draggable element -->
<div id="draggable" draggable="true" ondragstart="drag(event)">
    Drag me!
</div>

<!-- Drop zone -->
<div id="dropzone" ondrop="drop(event)" ondragover="allowDrop(event)">
    Drop here
</div>
```

### Event Handlers
- `ondragstart`: Fires when dragging starts
- `ondrag`: Fires while dragging
- `ondragend`: Fires when dragging ends
- `ondragenter`: Fires when dragged element enters a valid drop target
- `ondragover`: Fires while dragged element is over a valid drop target
- `ondragleave`: Fires when dragged element leaves a valid drop target
- `ondrop`: Fires when dragged element is dropped

### Data Transfer
```javascript
// Start dragging
function drag(e) {
    e.dataTransfer.setData("text", e.target.id);
}

// Allow dropping
function allowDrop(e) {
    e.preventDefault();
}

// Handle drop
function drop(e) {
    e.preventDefault();
    const data = e.dataTransfer.getData("text");
    e.target.appendChild(document.getElementById(data));
}
```

## Exercise
Create a drag and drop application that:
1. Allows dragging and dropping items
2. Implements sorting of items
3. Shows visual feedback during drag
4. Handles multiple drag zones
5. Implements undo functionality

Save your work as `exercise.html` in this folder.
