# Web Development Cheat Sheet
## Quick Reference Guide for HTML, CSS & JavaScript

---

## 🏗️ HTML Quick Reference

### Basic Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Content goes here -->
    <script src="script.js"></script>
</body>
</html>
```

### Common Tags

| Tag | Use | Example |
|-----|-----|---------|
| `<h1>` - `<h6>` | Headings | `<h1>Main Title</h1>` |
| `<p>` | Paragraph | `<p>Text here</p>` |
| `<a>` | Link | `<a href="url">Click</a>` |
| `<img>` | Image | `<img src="pic.jpg" alt="Pic">` |
| `<button>` | Button | `<button>Click</button>` |
| `<input>` | Input field | `<input type="text">` |
| `<div>` | Container | `<div>Content</div>` |
| `<span>` | Inline text | `<span>inline</span>` |
| `<ul>` | Unordered list | `<ul><li>Item</li></ul>` |
| `<ol>` | Ordered list | `<ol><li>Item</li></ol>` |
| `<form>` | Form | `<form>inputs</form>` |
| `<label>` | Form label | `<label for="id">Label</label>` |

### Semantic Tags
```html
<header>    <!-- Page/section header -->
<nav>       <!-- Navigation menu -->
<main>      <!-- Main content -->
<section>   <!-- Thematic section -->
<article>   <!-- Self-contained content -->
<aside>     <!-- Sidebar/related content -->
<footer>    <!-- Footer -->
```

### HTML Attributes
```html
id="unique-id"                  <!-- Unique identifier -->
class="class-name"              <!-- CSS class -->
style="color: red;"             <!-- Inline CSS -->
href="url"                       <!-- Link URL -->
src="image.jpg"                 <!-- Image source -->
alt="Description"               <!-- Image description -->
type="text"                      <!-- Input type -->
placeholder="Enter text"        <!-- Input placeholder -->
disabled                        <!-- Disable element -->
required                        <!-- Required field -->
```

---

## 🎨 CSS Quick Reference

### How to Apply CSS
```css
/* Element selector */
p { color: blue; }

/* Class selector */
.my-class { color: red; }

/* ID selector */
#my-id { color: green; }

/* Multiple selectors */
h1, h2, h3 { color: navy; }

/* Descendant selector */
.container p { font-size: 14px; }

/* Child selector */
.parent > .child { margin: 10px; }

/* Hover effect */
a:hover { color: orange; }

/* Focus (for inputs) */
input:focus { border-color: blue; }
```

### Text & Font Properties
```css
color: #333;                    /* Text color */
font-size: 16px;                /* Font size */
font-weight: bold;              /* Font weight (bold, normal, 100-900) */
font-family: Arial, sans-serif; /* Font family */
text-align: center;             /* Text alignment */
line-height: 1.5;               /* Line spacing */
text-decoration: underline;     /* Text decoration */
text-transform: uppercase;      /* Transform text */
letter-spacing: 2px;            /* Space between letters */
```

### Box Model Properties
```css
/* Margin (outside) */
margin: 20px;                   /* All sides */
margin: 10px 20px;              /* Top/Bottom Left/Right */
margin: 10px 20px 30px 40px;   /* Top Right Bottom Left */

/* Padding (inside) */
padding: 20px;

/* Border */
border: 2px solid #333;
border-radius: 8px;             /* Rounded corners */

/* Width & Height */
width: 100%;
height: 200px;
max-width: 1200px;
min-height: 100px;
```

### Background Properties
```css
background-color: #f0f0f0;
background-image: url('bg.jpg');
background-size: cover;         /* cover, contain, 100px, etc */
background-position: center;
background-repeat: no-repeat;   /* repeat, repeat-x, repeat-y */
opacity: 0.5;                   /* Transparency (0-1) */
```

### Display & Layout
```css
display: block;                 /* Full width */
display: inline;                /* Next to each other */
display: inline-block;          /* Inline + block features */
display: flex;                  /* Flexible layout */
display: grid;                  /* Grid layout */
display: none;                  /* Hide element */
visibility: hidden;             /* Hide but keep space */
```

### Flexbox (Most Important!)
```css
.container {
    display: flex;
    
    /* Direction */
    flex-direction: row;        /* row, column, row-reverse */
    
    /* Horizontal alignment */
    justify-content: center;    /* flex-start, flex-end, space-between, space-around */
    
    /* Vertical alignment */
    align-items: center;        /* flex-start, flex-end, stretch */
    
    /* Spacing */
    gap: 20px;
    
    /* Wrap */
    flex-wrap: wrap;
}

.item {
    flex: 1;                    /* Equal width */
    flex-basis: 200px;          /* Base width */
}
```

### Grid Layout
```css
.container {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr;    /* 3 columns */
    grid-template-rows: 100px 200px;       /* 2 rows */
    gap: 20px;                  /* Space between items */
    grid-auto-fit: minmax(300px, 1fr);    /* Responsive */
}
```

### Position Properties
```css
position: static;               /* Default */
position: relative;             /* Relative to normal position */
position: absolute;             /* Relative to parent */
position: fixed;                /* Fixed to viewport */

top: 10px;
right: 10px;
bottom: 10px;
left: 10px;
z-index: 10;                    /* Stacking order */
```

### Transform & Transition
```css
/* Transform */
transform: translate(10px, 20px);
transform: rotate(45deg);
transform: scale(1.5);
transform: skew(10deg);

/* Transition */
transition: all 0.3s ease;
transition-property: color;
transition-duration: 0.5s;
transition-timing-function: ease-in-out;
```

### Shadow & Effects
```css
box-shadow: 0 5px 15px rgba(0,0,0,0.1);
text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
filter: blur(5px);
filter: brightness(1.2);
filter: contrast(1.1);
```

### Media Queries (Responsive)
```css
/* Desktop first */
@media (max-width: 768px) {
    .container {
        flex-direction: column;
    }
}

@media (max-width: 480px) {
    .container {
        padding: 10px;
    }
}
```

### Color Values
```css
color: red;                     /* Named color */
color: #FF5733;                 /* Hex */
color: rgb(255, 87, 51);        /* RGB */
color: rgba(255, 87, 51, 0.5);  /* RGBA (with alpha) */
color: hsl(9, 100%, 60%);       /* HSL */
```

---

## ⚡ JavaScript Quick Reference

### Variables & Data Types
```javascript
// Variables (use let or const, not var)
let name = "Alice";             // String
let age = 25;                   /* Number */
let isStudent = true;           // Boolean
let fruits = ["apple", "banana"];  // Array
let person = {                  // Object
    name: "Bob",
    age: 30
};
const PI = 3.14159;             // Constant

// Access data
person.name;                    // "Bob"
person["name"];                 // "Bob"
fruits[0];                      // "apple"
```

### Operators
```javascript
// Arithmetic
+ - * / % (remainder)

// Assignment
= += -= *= /=

// Comparison
== (loose equal) === (strict equal)
!= !== < > <= >=

// Logical
&& (AND) || (OR) ! (NOT)

// String concatenation
"Hello" + " " + "World"
```

### String Methods
```javascript
let text = "Hello World";
text.length;                    // 11
text.toUpperCase();             // "HELLO WORLD"
text.toLowerCase();             // "hello world"
text.includes("World");         // true
text.indexOf("World");          // 6
text.replace("World", "JS");    // "Hello JS"
text.split(" ");                // ["Hello", "World"]
text.trim();                    // Remove whitespace
```

### Array Methods
```javascript
let arr = [1, 2, 3, 4, 5];

arr.length;                     // 5
arr[0];                         // 1
arr.push(6);                    // Add to end
arr.pop();                      // Remove from end
arr.shift();                    // Remove from start
arr.unshift(0);                 // Add to start
arr.includes(3);                // true
arr.indexOf(3);                 // 2
arr.join("-");                  // "1-2-3-4-5"
arr.map(x => x * 2);            // [2, 4, 6, 8, 10]
arr.filter(x => x > 2);         // [3, 4, 5]
```

### Conditionals
```javascript
// If statement
if (age >= 18) {
    console.log("Adult");
} else if (age >= 13) {
    console.log("Teen");
} else {
    console.log("Child");
}

// Ternary operator
let status = age >= 18 ? "Adult" : "Minor";

// Switch statement
switch (day) {
    case "Monday":
        console.log("Start of week");
        break;
    case "Friday":
        console.log("Almost weekend");
        break;
    default:
        console.log("Weekday");
}
```

### Loops
```javascript
// For loop
for (let i = 0; i < 5; i++) {
    console.log(i);
}

// While loop
while (count < 10) {
    count++;
}

// For...of loop (arrays)
for (let item of fruits) {
    console.log(item);
}

// For...in loop (objects)
for (let key in person) {
    console.log(key);
}

// Array forEach
arr.forEach(function(item) {
    console.log(item);
});
```

### Functions
```javascript
// Function declaration
function greet(name) {
    return "Hello, " + name;
}

greet("Alice");                 // "Hello, Alice"

// Arrow function (ES6)
const add = (a, b) => a + b;
add(5, 3);                      // 8

// Function with default parameter
function multiply(a, b = 1) {
    return a * b;
}

// Function that returns a function
function makeMultiplier(n) {
    return function(x) {
        return x * n;
    };
}
```

### DOM Manipulation
```javascript
// Get elements
document.getElementById("id");
document.querySelector(".class");
document.querySelector("p");
document.querySelectorAll("p");

// Change content
element.textContent = "New text";
element.innerHTML = "<b>Bold</b>";

// Change attributes
element.setAttribute("id", "new-id");
element.getAttribute("id");
element.removeAttribute("id");

// Change styles
element.style.color = "red";
element.style.fontSize = "18px";

// Classes
element.classList.add("active");
element.classList.remove("active");
element.classList.toggle("active");
element.classList.contains("active");

// Create & remove elements
let newDiv = document.createElement("div");
newDiv.textContent = "Hello";
document.body.appendChild(newDiv);
element.remove();
```

### Events
```javascript
// Click event
button.addEventListener("click", function() {
    console.log("Button clicked!");
});

// Input event
input.addEventListener("input", function(event) {
    console.log(event.target.value);
});

// Form submission
form.addEventListener("submit", function(event) {
    event.preventDefault();     // Stop page reload
    console.log("Form submitted");
});

// Key press
document.addEventListener("keypress", function(event) {
    console.log(event.key);
});

// Mouse events
element.addEventListener("mouseover", function() {});
element.addEventListener("mouseout", function() {});

// Common event properties
event.target;                   // Element that triggered event
event.preventDefault();         // Prevent default behavior
event.stopPropagation();        // Stop event bubbling
```

### Common Event Types
```javascript
"click"         // Click
"dblclick"      // Double click
"input"         // Input changed
"change"        // Value changed
"submit"        // Form submitted
"focus"         // Element focused
"blur"          // Element lost focus
"keydown"       // Key pressed
"keyup"         // Key released
"mouseover"     // Mouse over
"mouseout"      // Mouse left
"load"          // Page loaded
"scroll"        // Page scrolled
```

### Timers
```javascript
// Run code after delay
setTimeout(function() {
    console.log("Runs after 2 seconds");
}, 2000);

// Run code repeatedly
let interval = setInterval(function() {
    console.log("Runs every 1 second");
}, 1000);

// Stop interval
clearInterval(interval);
```

### Useful Methods
```javascript
console.log("Message");         // Log message
console.error("Error");         // Log error
console.warn("Warning");        // Log warning

parseInt("42");                 // Convert to integer
parseFloat("3.14");             // Convert to float
String(42);                     // Convert to string
Boolean(1);                     // Convert to boolean

Math.random();                  // Random 0-1
Math.round(4.6);                // 5
Math.max(1, 5, 3);              // 5
Math.min(1, 5, 3);              // 1
Math.abs(-5);                   // 5

JSON.stringify(obj);            // Object to JSON string
JSON.parse(jsonString);         // JSON string to object
```

---

## 📋 Common Patterns

### Hide/Show Element
```javascript
// Hide
element.style.display = "none";

// Show
element.style.display = "block"; // or "flex", "inline", etc

// Toggle
element.classList.toggle("hidden");
```

### Toggle Class
```javascript
button.addEventListener("click", function() {
    element.classList.toggle("active");
});
```

### Form Input Values
```javascript
let input = document.getElementById("name");
let value = input.value;        // Get value
input.value = "New value";      // Set value
input.value = "";               // Clear input
```

### Conditional Class
```javascript
if (isActive) {
    element.classList.add("active");
} else {
    element.classList.remove("active");
}
```

### Loop Through Elements
```javascript
let buttons = document.querySelectorAll(".btn");

buttons.forEach(function(button) {
    button.addEventListener("click", function() {
        console.log("Clicked!");
    });
});
```

---

## 🎯 Tips & Best Practices

### HTML
- ✅ Use semantic tags (header, nav, main, footer)
- ✅ Use meaningful IDs and classes
- ✅ Always include alt text for images
- ✅ Use labels for form inputs
- ✅ Validate HTML with validator.w3.org

### CSS
- ✅ Use flexbox for layouts
- ✅ Mobile-first approach
- ✅ Use CSS variables for colors
- ✅ Keep selectors specific but not too long
- ✅ Test on mobile devices

### JavaScript
- ✅ Use meaningful variable names
- ✅ Use `let` or `const`, not `var`
- ✅ Validate form inputs
- ✅ Test in console (F12)
- ✅ Keep code DRY (Don't Repeat Yourself)

---

## 🚀 Resources

- **MDN Web Docs:** https://developer.mozilla.org/
- **Can I Use:** https://caniuse.com/ (Browser compatibility)
- **Color Picker:** https://coolors.co/
- **Fonts:** https://fonts.google.com/
- **Icons:** https://fontawesome.com/

---

**Keep this handy while learning! 📚**
