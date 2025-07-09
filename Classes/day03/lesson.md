# Day 3: Semantic HTML5 and Accessibility

## What is Semantic HTML?
Semantic HTML means using HTML elements for their intended purpose. This makes your code more meaningful and helps with:
- Search Engine Optimization (SEO)
- Accessibility
- Code maintainability
- Better structure

## New Semantic Elements in HTML5

### Document Structure
- `<header>`: Contains introductory content or navigation
- `<nav>`: Contains navigation links
- `<main>`: Contains main content of the document
- `<article>`: Independent, self-contained content
- `<section>`: Thematic grouping of content
- `<aside>`: Content related to the main content
- `<footer>`: Footer content for the document or section

### Media Elements
- `<figure>`: Self-contained content (usually images, diagrams, photos, code snippets)
- `<figcaption>`: Caption for a figure

### Form Elements
- `<fieldset>`: Groups related form elements
- `<legend>`: Caption for a fieldset

### Example of Semantic Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Blog</title>
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <article>
            <h1>Blog Post Title</h1>
            <p>Blog post content...</p>
        </article>

        <aside>
            <h2>Related Posts</h2>
            <ul>
                <li><a href="#post1">Post 1</a></li>
                <li><a href="#post2">Post 2</a></li>
            </ul>
        </aside>
    </main>

    <footer>
        <p>&copy; 2025 My Blog. All rights reserved.</p>
    </footer>
</body>
</html>
```

## Accessibility Best Practices
1. Use proper heading hierarchy (h1-h6)
2. Add `alt` text to images
3. Use semantic elements
4. Add `aria-label` for screen readers
5. Make links descriptive
6. Use proper form labels

## Exercise
Create a semantic HTML5 document that includes:
1. A blog post with proper structure
2. Navigation menu
3. Related posts section
4. Footer with copyright
5. Images with proper alt text
6. Form for comments

Save your work as `exercise.html` in this folder.
