# Day 19: Accessibility (a11y) & ARIA

## Overview
Accessibility (often abbreviated as a11y) ensures that web content is usable by everyone, including people with disabilities. HTML5 and ARIA (Accessible Rich Internet Applications) provide powerful tools to build accessible, inclusive web applications.

---

## 1. Semantic HTML
Semantic HTML uses elements that convey meaning and structure (like `<nav>`, `<main>`, `<header>`, `<footer>`, `<form>`, `<button>`, etc.). This helps screen readers and assistive technologies understand your content.

**Example:**
```html
<nav aria-label="Main navigation">
  <a href="#home">Home</a>
  <a href="#about">About</a>
  <a href="#contact">Contact</a>
</nav>
```

**Best for:** Landmarks, navigation, forms, and any structural content.

---

## 2. Keyboard Navigation
All interactive elements should be usable by keyboard alone. This means:
- Use `<button>`, `<a>`, `<input>`, etc., which are focusable by default.
- Manage focus order with `tabindex` if needed.
- Provide visible focus styles.
- Support navigation with Tab, Arrow keys, Enter, and Space.

**Example:** Tabs component with keyboard support.

---

## 3. ARIA Roles & Attributes
ARIA attributes supplement HTML to improve accessibility, especially for custom components.
- `role`: Defines the type of widget (e.g., `tablist`, `tab`, `tabpanel`).
- `aria-label`, `aria-labelledby`: Provide accessible names.
- `aria-selected`, `aria-controls`: Indicate state and relationships.

**Example:**
```html
<div class="tabs" role="tablist" aria-label="Sample Tabs">
  <button role="tab" aria-selected="true" aria-controls="tabpanel-1" id="tab-1">Tab 1</button>
  <button role="tab" aria-selected="false" aria-controls="tabpanel-2" id="tab-2">Tab 2</button>
</div>
<div role="tabpanel" id="tabpanel-1" aria-labelledby="tab-1">Tab 1 content...</div>
```

---

## 4. Accessibility Testing
- **Keyboard:** Use Tab, Shift+Tab, and Arrow keys to navigate.
- **Screen Reader:** Try NVDA (Windows), VoiceOver (Mac), or Narrator (Windows).
- **Browser Tools:** Use accessibility inspectors (e.g., Chrome DevTools > Accessibility panel).

---

## Best Practices
- Always use semantic HTML first; use ARIA only when necessary.
- Provide visible focus indicators.
- Use descriptive link/button text.
- Test with keyboard and screen reader.
- Avoid "click here" and ambiguous labels.

## Resources
- [MDN: Accessibility](https://developer.mozilla.org/en-US/docs/Web/Accessibility)
- [WAI-ARIA Authoring Practices](https://www.w3.org/WAI/ARIA/apg/)
- [WebAIM: Keyboard Accessibility](https://webaim.org/techniques/keyboard/)

---

**Next:** Try the exercise and solution files to practice making your web content accessible to all users!
