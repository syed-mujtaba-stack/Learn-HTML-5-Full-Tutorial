# Day 4: HTML5 Forms and Input Types

## HTML5 Forms Basics
Forms are used to collect user input. The basic structure is:

```html
<form action="submit.php" method="post">
    <!-- Form elements go here -->
</form>
```

### Form Attributes
- `action`: URL where to send form data
- `method`: HTTP method (get/post)
- `enctype`: Encoding type for form data
- `autocomplete`: Enable/disable autocomplete
- `novalidate`: Disable browser validation

## Input Types in HTML5

### Basic Input Types
- `text`: Regular text input
- `password`: Password input (characters hidden)
- `email`: Email address input (validates email format)
- `tel`: Telephone number input
- `url`: URL input (validates URL format)
- `number`: Numeric input
- `date`: Date picker
- `time`: Time picker
- `color`: Color picker
- `range`: Slider input
- `search`: Search box
- `file`: File upload

### New HTML5 Input Types
- `datetime-local`: Date and time picker
- `month`: Month picker
- `week`: Week picker
- `search`: Search box with magnifying glass
- `color`: Color picker

### Form Controls
- `<button>`: Clickable button
- `<input type="submit">`: Submit button
- `<input type="reset">`: Reset button
- `<textarea>`: Multi-line text input
- `<select>`: Dropdown menu
- `<option>`: Option in dropdown
- `<datalist>`: Dropdown list for input suggestions

## Form Validation
- `required`: Field must be filled
- `min`/`max`: Minimum/maximum value
- `minlength`/`maxlength`: Minimum/maximum length
- `pattern`: Regular expression pattern
- `step`: Value increment
- `multiple`: Allow multiple file uploads

## Exercise
Create an HTML5 form that includes:
1. Personal information section (name, email, phone)
2. Date of birth using date picker
3. Color preference using color picker
4. Favorite number using range slider
5. Address section with street, city, state, zip
6. File upload for profile picture
7. Submit and Reset buttons

Save your work as `exercise.html` in this folder.
