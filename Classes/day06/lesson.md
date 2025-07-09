# Day 6: HTML5 Canvas and Graphics

## Introduction to Canvas
The `<canvas>` element is used to draw graphics via JavaScript.

### Basic Canvas Setup
```html
<canvas id="myCanvas" width="500" height="500">
    Your browser does not support the canvas element.
</canvas>
```

### Drawing Basics
```javascript
const canvas = document.getElementById('myCanvas');
const ctx = canvas.getContext('2d');

// Draw a rectangle
ctx.fillStyle = '#FF0000';
ctx.fillRect(10, 10, 100, 100);

// Draw a circle
ctx.beginPath();
ctx.arc(150, 150, 50, 0, Math.PI * 2);
ctx.fillStyle = '#00FF00';
ctx.fill();
```

### Canvas Methods
- `fillRect(x, y, width, height)`: Draws filled rectangle
- `strokeRect(x, y, width, height)`: Draws rectangle outline
- `arc(x, y, radius, startAngle, endAngle)`: Draws circle/arc
- `beginPath()`: Starts a new path
- `closePath()`: Closes the current path
- `stroke()`: Draws the outline of shapes
- `fill()`: Fills the shapes with color

### Canvas Properties
- `fillStyle`: Color for filling shapes
- `strokeStyle`: Color for stroke
- `lineWidth`: Width of lines
- `font`: Font for text

## Exercise
Create an HTML5 canvas that demonstrates:
1. Drawing basic shapes (rectangle, circle, line)
2. Using different colors and styles
3. Creating a simple animation
4. Drawing text
5. Using event listeners for interaction

Save your work as `exercise.html` in this folder.
