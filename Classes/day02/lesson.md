# Day 2: Lists, Tables, and Basic Formatting

## Lists in HTML5
There are three types of lists in HTML5:

### 1. Unordered List (`<ul>`)
- Used for items without specific order
- Each item starts with `<li>`
- Example:
```html
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>
```

### 2. Ordered List (`<ol>`)
- Used for items with specific order
- Items are automatically numbered
- Example:
```html
<ol>
    <li>First step</li>
    <li>Second step</li>
    <li>Third step</li>
</ol>
```

### 3. Description List (`<dl>`, `<dt>`, `<dd>`)
- Used for terms and their descriptions
- `<dt>` for term
- `<dd>` for description
- Example:
```html
<dl>
    <dt>HTML5</dt>
    <dd>A markup language for structuring and presenting content on the web</dd>
    <dt>CSS</dt>
    <dd>A style sheet language used for describing the look and formatting of a document</dd>
</dl>
```

## Tables in HTML5
Tables are used to display tabular data.

### Basic Table Structure
```html
<table>
    <tr> <!-- Table Row -->
        <th> <!-- Table Header -->
            Header Text
        </th>
    </tr>
    <tr>
        <td> <!-- Table Data -->
            Data Cell
        </td>
    </tr>
</table>
```

### Table Attributes
- `border`: Adds border to table
- `colspan`: Spans multiple columns
- `rowspan`: Spans multiple rows
- `caption`: Adds a caption to the table

## Basic Formatting Tags
- `<strong>`: Bold text
- `<em>`: Italic text
- `<mark>`: Highlighted text
- `<small>`: Smaller text
- `<del>`: Strikethrough text
- `<ins>`: Underlined text

## Exercise
Create an HTML5 document that includes:
1. A recipe list using ordered list
2. A shopping list using unordered list
3. A glossary using description list
4. A table showing:
   - Product name
   - Price
   - Quantity
   - Total
5. Use formatting tags to make the text more readable

Save your work as `exercise.html` in this folder.
