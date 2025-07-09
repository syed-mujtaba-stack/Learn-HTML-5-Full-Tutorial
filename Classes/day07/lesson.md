# Day 7: SVG Graphics

## What is SVG?
SVG stands for Scalable Vector Graphics. It's an XML-based vector image format for 2D graphics.

### Basic SVG Elements
- `<circle>`: Draws a circle
- `<rect>`: Draws a rectangle
- `<ellipse>`: Draws an ellipse
- `<line>`: Draws a line
- `<polyline>`: Draws multiple connected lines
- `<polygon>`: Draws a closed shape
- `<path>`: Draws complex shapes

### SVG Attributes
- `width`/`height`: Dimensions of SVG
- `viewBox`: Defines coordinate system
- `fill`: Fill color
- `stroke`: Border color
- `stroke-width`: Border width
- `cx`/`cy`: Center coordinates
- `r`: Radius

### Example SVG
```html
<svg width="200" height="200" viewBox="0 0 200 200">
    <circle cx="50" cy="50" r="40" fill="red" />
    <rect x="100" y="20" width="80" height="60" fill="blue" />
    <line x1="10" y1="10" x2="190" y2="190" stroke="black" stroke-width="2" />
</svg>
```

## Exercise
Create an SVG illustration that includes:
1. Multiple shapes (circle, rectangle, line)
2. Different colors and styles
3. A gradient
4. Animation using SMIL
5. Responsive SVG

Save your work as `exercise.html` in this folder.
