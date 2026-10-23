Assignment 5.2 — CSS Selectors Practice

Objective

To create a webpage using different CSS selectors and understand how CSS cascade and specificity work.

Question 1: Create at least 5 HTML elements.

Answer:

The following HTML code contains headings, paragraphs, a navigation bar, sections, links, and cards.

HTML File ("index.html")

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Selectors Practice</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>Welcome to My Website</h1>
        <p>This webpage demonstrates different CSS selectors.</p>
    </header>

    <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
    </nav>

    <section id="home">
        <h2>Home Section</h2>
        <p>This is the home section of my webpage.</p>
    </section>

    <section id="about">
        <h2>About Us</h2>
        <p class="highlight">We are learning HTML and CSS.</p>
    </section>

    <section id="services">
        <h2>Our Services</h2>

        <div class="card">
            <h3>HTML</h3>
            <p>HTML is used to create webpage structure.</p>
        </div>

        <div class="card">
            <h3>CSS</h3>
            <p>CSS is used to style webpages.</p>
        </div>
    </section>

    <footer>
        <p>Created for CSS Selectors Practice.</p>
    </footer>

</body>
</html>

Question 2: Style headings or paragraphs using an element selector.

Answer:

An element selector selects all HTML elements of a particular type.

Example:

h1 {
    color: blue;
}

p {
    font-size: 16px;
}

This CSS makes all "h1" headings blue and sets all paragraphs to a font size of 16 pixels.

Question 3: Style multiple cards or sections using a class selector.

Answer:

A class selector is used to style multiple elements with the same class name. It begins with a dot (".").

Example:

.card {
    background-color: white;
    padding: 20px;
    margin: 10px;
    border-radius: 8px;
    box-shadow: 0 2px 5px #cccccc;
}

.highlight {
    color: green;
    font-weight: bold;
}

Both cards receive the same styling because they use the "card" class.

Question 4: Style a specific section using an ID selector.

Answer:

An ID selector styles a specific HTML element using its unique ID. It begins with a hash ("#").

Example:

#home {
    background-color: #eaf2f8;
    padding: 20px;
}

This CSS applies the background color and padding only to the element with "id="home"".

Question 5: Use the universal selector appropriately.

Answer:

The universal selector ("*") selects all HTML elements.

Example:

* {
    box-sizing: border-box;
}

This ensures that padding and borders are included in an element's specified width and height.

Question 6: Use a grouping selector.

Answer:

A grouping selector applies the same CSS rules to multiple selectors by separating them with commas.

Example:

h1, h2, h3 {
    font-family: Arial, sans-serif;
    color: #1a5276;
}

This applies the same font family and text color to all "h1", "h2", and "h3" headings.

Question 7: Create two conflicting CSS rules and observe cascade and specificity.

Answer:

Example:

p {
    color: blue;
}

.highlight {
    color: red;
}

HTML:

<p class="highlight">This is a highlighted paragraph.</p>

Observation:

The paragraph appears red because a class selector has higher specificity than an element selector. Therefore, ".highlight" overrides the "p" rule, even though both rules have the same importance.

If two rules have equal specificity, the rule appearing later in the stylesheet generally takes precedence.

Complete CSS File ("style.css")

/* Universal Selector */
* {
    box-sizing: border-box;
}

/* Element Selectors */
body {
    font-family: Arial, sans-serif;
    background-color: #f4f7fa;
    color: #333333;
    margin: 0;
    padding: 20px;
}

h1 {
    color: blue;
    text-align: center;
}

p {
    font-size: 16px;
    line-height: 1.6;
}

/* Grouping Selector */
h1, h2, h3 {
    font-family: Arial, sans-serif;
}

/* Navigation Styling */
nav {
    background-color: #1a5276;
    padding: 15px;
    text-align: center;
}

nav a {
    color: white;
    text-decoration: none;
    margin: 0 12px;
    font-weight: bold;
}

/* ID Selector */
#home {
    background-color: #eaf2f8;
    padding: 20px;
}

/* Class Selector */
.card {
    background-color: white;
    padding: 20px;
    margin: 10px 0;
    border-radius: 8px;
    box-shadow: 0 2px 5px #cccccc;
}

.highlight {
    color: red;
    font-weight: bold;
}

/* Footer Styling */
footer {
    text-align: center;
    margin-top: 20px;
    padding: 10px;
    background-color: #dddddd;
}

Explanation of CSS Selectors

Selector| Example| Purpose
Element| "p"| Selects all paragraphs
Class| ".card"| Selects all elements with the card class
ID| "#home"| Selects the element with the home ID
Universal| "*"| Selects all elements
Grouping| "h1, h2, h3"| Applies common rules to multiple selectors

Result

The webpage was created successfully using different CSS selectors. Element, class, ID, universal, and grouping selectors were implemented. Conflicting CSS rules were also tested to understand the cascade and specificity.

Conclusion

This assignment helped me understand how different CSS selectors work and how they can be used to style HTML elements. I also learned how CSS specificity and the cascade determine which styling rule is applied when multiple rules conflict.

Submission

1. "index.html" — Contains the HTML webpage.
2. "style.css" — Contains all CSS styling rules.
3. "Assignment-5.2.md" — Contains the questions, answers, selector explanations, result, and conclusion.