# Day 17: Web Animations API & CSS Animations

## Overview
Modern web applications use animation to enhance user experience, provide feedback, and create engaging interfaces. HTML5 offers two main approaches:
- **CSS Animations and Transitions**: Declarative, simple, and efficient for most UI effects.
- **Web Animations API (WAAPI)**: JavaScript-driven, powerful, and interactive for advanced or dynamic animations.

---

## CSS Transitions
Transitions animate changes in CSS properties when an element’s state changes (e.g., on `:hover`).

```css
.box {
  transition: transform 0.5s, background 0.3s;
}
.box:hover {
  background: #28a745;
  transform: scale(1.2) rotate(10deg);
}
```

**Best for:** Simple, state-based effects (hover, focus, active).

---

## CSS Keyframes Animations
Keyframes allow complex, multi-step animations.

```css
@keyframes bounce {
  0%   { transform: translateY(0); }
  30%  { transform: translateY(-60px) scale(1.2); }
  50%  { transform: translateY(0) scale(1); }
  70%  { transform: translateY(-30px) scale(1.1); }
  100% { transform: translateY(0); }
}
.box.animate {
  animation: bounce 1s ease-in-out;
}
```

**Best for:** Reusable, timeline-based animations (entrances, exits, attention effects).

---

## Web Animations API (WAAPI)
The Web Animations API enables you to animate elements with JavaScript for full control.

### Basic Usage
```js
const box = document.querySelector('.box');
const animation = box.animate([
  { transform: 'translateX(0) scale(1)', background: '#007bff' },
  { transform: 'translateX(240px) scale(1.5)', background: '#ffc107' },
  { transform: 'translateX(0) scale(1)', background: '#007bff' }
], {
  duration: 2000,
  iterations: 1,
  fill: 'forwards',
  easing: 'cubic-bezier(.68,-0.55,.27,1.55)'
});
```

### Controlling Animations
- `animation.play()` — Play/resume
- `animation.pause()` — Pause
- `animation.reverse()` — Reverse direction
- `animation.cancel()` — Stop and reset
- `animation.finished.then(...)` — Callback when done

**Best for:**
- Complex, interactive, or programmatically controlled effects
- Synchronizing multiple animations
- Animating properties not available in CSS

---

## When to Use Each Approach
- **CSS**: For simple, performance-critical, or state-based UI effects.
- **WAAPI**: For advanced, dynamic, or interactive animations (e.g., games, custom controls, animation timelines).

---

## Resources
- [MDN: CSS Transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_transitions/Using_CSS_transitions)
- [MDN: CSS Animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations)
- [MDN: Web Animations API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Animations_API)

---

**Next:** Try the exercise and solution files for hands-on practice with both CSS and JavaScript-powered animations!
