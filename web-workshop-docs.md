# Web Development Fundamentals Workshop
## IET On Campus - Web Development 101

**Duration:** 2 hours | **Level:** Complete Beginners | **Facilitator:** Mohamed Abdalla

---

## 📚 Table of Contents
1. [Introduction](#introduction)
2. [HTML Fundamentals](#html-fundamentals)
3. [CSS Fundamentals](#css-fundamentals)
4. [JavaScript Basics](#javascript-basics)
5. [Resources & Next Steps](#resources--next-steps)

---

## Introduction

### What is Web Development?
Web development is creating websites and web applications. Every website you visit is made of three core technologies:

- **HTML** - The structure (skeleton)
- **CSS** - The styling & layout (clothes)
- **JavaScript** - The interactivity (movement & behavior)

### The Goal Today
By the end of this workshop, you'll understand how these three work together and build a simple interactive webpage.

---

## HTML Fundamentals

### What is HTML?
**HTML** (HyperText Markup Language) is the foundation of all web pages. It provides structure and content.

Think of it like the skeleton of a building—it holds everything in place.

### Basic HTML Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Webpage</title>
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>This is a paragraph.</p>
</body>
</html>
```

**Key parts:**
- `<!DOCTYPE html>` - Tells the browser this is an HTML5 file
- `<head>` - Contains metadata (info about the page, title, styles)
- `<body>` - Contains all visible content

### Common HTML Tags

| Tag | Purpose | Example |
|-----|---------|---------|
| `<h1>` to `<h6>` | Headings (h1 = largest) | `<h1>Main Title</h1>` |
| `<p>` | Paragraph | `<p>This is text.</p>` |
| `<br>` | Line break | `Line 1<br>Line 2` |
| `<div>` | Container/section | `<div>Content here</div>` |
| `<a>` | Hyperlink | `<a href="url">Click me</a>` |
| `<img>` | Image | `<img src="image.jpg" alt="Description">` |
| `<button>` | Clickable button | `<button>Click me</button>` |
| `<input>` | Input field | `<input type="text">` |
| `<ul>` / `<ol>` | Unordered/Ordered lists | `<ul><li>Item</li></ul>` |

### Semantic HTML (Best Practice)

Use semantic tags to give meaning to your content:

| Semantic Tag | Purpose |
|--------------|---------|
| `<header>` | Page/section header |
| `<nav>` | Navigation menu |
| `<main>` | Main content |
| `<section>` | Thematic section |
| `<article>` | Self-contained content |
| `<footer>` | Page/section footer |

```html
<header>
    <nav>
        <a href="/">Home</a>
        <a href="/about">About</a>
    </nav>
</header>

<main>
    <article>
        <h1>Article Title</h1>
        <p>Article content...</p>
    </article>
</main>

<footer>
    <p>&copy; 2024 My Website</p>
</footer>
```

---

## CSS Fundamentals

### What is CSS?
**CSS** (Cascading Style Sheets) controls the visual appearance and layout of HTML elements.

Think of it like putting clothes and makeup on—it makes things look beautiful!

### How to Add CSS

**Method 1: Inline (not recommended)**
```html
<p style="color: blue; font-size: 18px;">Styled text</p>
```

**Method 2: Internal (in <head>)**
```html
<head>
    <style>
        p {
            color: blue;
            font-size: 18px;
        }
    </style>
</head>
```

**Method 3: External (best practice)**
```html
<head>
    <link rel="stylesheet" href="style.css">
</head>
```

In `style.css`:
```css
p {
    color: blue;
    font-size: 18px;
}
```

### CSS Selectors

```css
/* Element selector - targets all <p> tags */
p {
    color: blue;
}

/* Class selector - targets elements with class="highlight" */
.highlight {
    background-color: yellow;
}

/* ID selector - targets element with id="main" */
#main {
    width: 800px;
}

/* Multiple selectors */
h1, h2, h3 {
    color: navy;
}

/* Descendant selector */
.container p {
    font-size: 16px;
}
```

### Common CSS Properties

```css
/* Text & Font */
color: #333;                    /* Text color */
font-size: 16px;                /* Text size */
font-weight: bold;              /* Font weight */
text-align: center;             /* Text alignment */

/* Box Model */
margin: 20px;                   /* Space outside element */
padding: 10px;                  /* Space inside element */
border: 2px solid #333;         /* Border */
width: 200px;                   /* Width */
height: 100px;                  /* Height */

/* Background */
background-color: #f0f0f0;      /* Background color */
background-image: url('bg.jpg');/* Background image */

/* Display & Layout */
display: block;                 /* Block (full width) */
display: inline;                /* Inline (next to each other) */
display: flex;                  /* Flexible box layout */

/* Positioning */
position: relative;             /* Relative to normal flow */
position: absolute;             /* Relative to parent */
top: 10px;                      /* Distance from top */
```

### The CSS Box Model

Every element is a box with:
```
┌─────────────────────────────────┐
│          margin                 │
│  ┌──────────────────────────┐   │
│  │      border              │   │
│  │  ┌────────────────────┐  │   │
│  │  │  padding           │  │   │
│  │  │ ┌────────────────┐ │  │   │
│  │  │ │    content     │ │  │   │
│  │  │ └────────────────┘ │  │   │
│  │  └────────────────────┘  │   │
│  └──────────────────────────┘   │
└─────────────────────────────────┘
```

### Flexbox (Modern Layout)

Flexbox makes creating responsive layouts easy:

```css
.container {
    display: flex;
    justify-content: center;        /* Align items horizontally */
    align-items: center;            /* Align items vertically */
    gap: 20px;                      /* Space between items */
}
```

**Common Flexbox Properties:**
- `justify-content: flex-start | center | flex-end | space-between | space-around`
- `align-items: flex-start | center | flex-end | stretch`
- `flex-direction: row | column`
- `gap: 20px` (space between items)

---

## JavaScript Basics

### What is JavaScript?
**JavaScript** (JS) adds interactivity to web pages. It makes things happen when users interact with the page.

Think of it like giving the webpage a brain—it can think, respond, and remember!

### Why Learn JavaScript?
- React to user clicks/input
- Update content dynamically
- Validate forms
- Create animations
- Build full web applications

### Your First JavaScript

```javascript
// This is a comment

// Log a message to the console
console.log("Hello, World!");

// Create a variable
let name = "Alice";
console.log(name);

// Simple math
let age = 20;
let nextYear = age + 1;
console.log(nextYear);
```

### Variables & Data Types

```javascript
// String (text)
let greeting = "Hello";

// Number (integer or decimal)
let count = 42;
let price = 19.99;

// Boolean (true/false)
let isStudent = true;

// Array (list of values)
let fruits = ["apple", "banana", "orange"];
console.log(fruits[0]); // "apple"

// Object (collection of key-value pairs)
let person = {
    name: "Bob",
    age: 25,
    isStudent: true
};
console.log(person.name); // "Bob"
```

### Functions

Functions are reusable blocks of code:

```javascript
// Define a function
function greet(name) {
    console.log("Hello, " + name);
}

// Call (use) the function
greet("Alice");  // Output: "Hello, Alice"

// Function that returns a value
function add(a, b) {
    return a + b;
}

let result = add(5, 3);  // result = 8
```

### Events & Interactivity

Listen for user actions and respond:

```html
<!-- HTML -->
<button id="myButton">Click me</button>
<p id="message"></p>

<script>
// Get the button element
let button = document.getElementById("myButton");
let message = document.getElementById("message");

// Listen for a click
button.addEventListener("click", function() {
    message.textContent = "Button was clicked!";
    message.style.color = "red";
});
</script>
```

### Common DOM Methods

```javascript
// Get elements
document.getElementById("id")           // Get by ID
document.querySelector(".class")        // Get by selector
document.querySelectorAll("p")          // Get multiple elements

// Change content
element.textContent = "New text";       // Change text
element.innerHTML = "<b>Bold</b>";      // Change HTML
element.style.color = "blue";           // Change style

// Add/Remove classes
element.classList.add("active");
element.classList.remove("active");
element.classList.toggle("active");
```


**Hint:**
```javascript
let button = document.getElementById("toggleButton");
let content = document.getElementById("content");

button.addEventListener("click", function() {
    // Toggle visibility
    if (content.style.display === "none") {
        content.style.display = "block";
    } else {
        content.style.display = "none";
    }
});
```

---

## Resources & Next Steps

### Continue Learning

**Free Resources:**
- **MDN Web Docs** (mozilla.org/en-US/docs/Web) - Gold standard documentation
- **freeCodeCamp** (freecodecamp.org) - Free interactive courses
- **Codecademy** - Interactive lessons
- **W3Schools** - Quick reference
- **GitHub** (github.com) - Explore projects, learn from others

### Next Topics to Explore
1. **Responsive Design** - Make sites work on mobile, tablet, desktop
2. **Advanced CSS** - Animations, Grid, advanced Flexbox
3. **JavaScript ES6+** - Modern JavaScript features
4. **Git & GitHub** - Version control (essential for developers!)
5. **Frameworks** - React, Vue, or Angular
6. **Backend** - Node.js, Python, databases

### Practice Projects
- Build a personal portfolio website
- Create a to-do list app (with localStorage)
- Build a weather app (using APIs)
- Make a calculator
- Create a simple game (rock-paper-scissors)

### IET On Campus
- Keep attending workshops
- Work on projects together
- Build your portfolio
- Network with other tech enthusiasts

---

## Useful Links

- **Visual Studio Code:** https://code.visualstudio.com/
- **MDN Web Docs:** https://developer.mozilla.org/
- **Can I Use (Browser Compatibility):** https://caniuse.com/
- **Color Picker:** https://coolors.co/
- **Font Library:** https://fonts.google.com/

---

**Happy Coding! 🚀**

Questions? Ask during Q&A or reach out on the IET Discord!
