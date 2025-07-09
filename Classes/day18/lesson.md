# Day 18: Responsive Images & Picture Element

## Overview
Responsive images are essential for modern web development. They ensure that users on any device, with any screen size or resolution, get the best visual experience and performance. HTML5 provides several features to help:
- `srcset` and `sizes` on `<img>`
- The `<picture>` element for art direction
- The `loading="lazy"` attribute for performance

---

## 1. Responsive Images with `srcset` and `sizes`
The `srcset` attribute allows you to specify multiple image sources for different resolutions. The `sizes` attribute tells the browser how much space the image will take up, so it can pick the best source.

```html
<img
  src="cat-400.jpg"
  srcset="cat-400.jpg 400w, cat-800.jpg 800w"
  sizes="(max-width: 600px) 100vw, 600px"
  alt="A Cat">
```
- **400w, 800w**: Image widths in pixels.
- **sizes**: How wide the image will display (e.g., 100vw = full viewport width).

**Best for:** Serving the right image resolution for different devices.

---

## 2. Art Direction with `<picture>`
The `<picture>` element allows you to swap images entirely based on media queries, not just resolution. This is useful for showing a different crop or composition on mobile vs. desktop.

```html
<picture>
  <source media="(max-width: 600px)" srcset="cat-mobile.jpg">
  <img src="cat-desktop.jpg" alt="Art Direction Example">
</picture>
```
- The browser uses the first matching `<source>`, falling back to `<img>` if none match.

**Best for:** Art direction (different crops, compositions, or even file formats).

---

## 3. Lazy Loading Images
The `loading="lazy"` attribute defers loading images until they scroll into view, improving performance and saving bandwidth.

```html
<img src="cat.jpg" loading="lazy" alt="Lazy Cat">
```

**Best for:** Offscreen images, long pages, galleries.

---

## Best Practices
- Always provide descriptive `alt` text.
- Use responsive images for all non-iconic content.
- Test on multiple devices and network speeds.
- Combine with CSS for flexible layouts.

## Resources
- [MDN: Responsive Images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)
- [MDN: `<picture>` element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture)
- [MDN: Lazy loading images](https://developer.mozilla.org/en-US/docs/Web/Performance/Lazy_loading)

---

**Next:** Try the exercise and solution files to practice responsive images, art direction, and lazy loading in HTML5!
