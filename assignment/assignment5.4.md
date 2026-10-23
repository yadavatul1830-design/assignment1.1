Assignment 5.4 — CSS Variables & Design Tokens

Objective

To create a small design system using reusable CSS variables for colors, spacing, and font sizes.

Question 1: Define CSS variables in ":root".

Answer:

CSS variables are reusable values that can be defined once and used throughout a stylesheet. The ":root" selector defines variables globally.

Example:

:root {
    --primary-color: #2563eb;
    --secondary-color: #14b8a6;
    --background-color: #f3f4f6;
    --text-color: #1f2937;
}

Question 2: Set primary color, secondary color, background color, and text color.

Answer:

The following variables define the main colors used in the design system.

:root {
    --primary-color: #2563eb;
    --secondary-color: #14b8a6;
    --background-color: #f3f4f6;
    --text-color: #1f2937;
}

- Primary color: Used for buttons and important headings.
- Secondary color: Used for accents and supporting elements.
- Background color: Used for the webpage background.
- Text color: Used for readable body text.

Question 3: Define small, medium, and large spacing variables.

Answer:

Spacing variables help maintain consistent gaps and padding throughout the webpage.

:root {
    --spacing-small: 8px;
    --spacing-medium: 16px;
    --spacing-large: 32px;
}

These variables can be reused for margins, padding, and gaps.

Question 4: Create font-size variables.

Answer:

Font-size variables help maintain a consistent typography system.

:root {
    --font-small: 14px;
    --font-medium: 18px;
    --font-large: 32px;
}

The variables can be used for paragraphs, buttons, and headings.

Question 5: Use variables in buttons, headings, and cards.

Answer:

CSS variables can be used with the "var()" function.

Example:

button {
    background-color: var(--primary-color);
    padding: var(--spacing-small) var(--spacing-medium);
    font-size: var(--font-medium);
}

h1 {
    color: var(--primary-color);
    font-size: var(--font-large);
}

.card {
    background-color: white;
    color: var(--text-color);
    padding: var(--spacing-large);
    margin-bottom: var(--spacing-medium);
}

This makes the design consistent and easier to maintain.

Question 6: Change a variable and verify that multiple elements update.

Answer:

To test CSS variables, change the primary color in the ":root" selector.

Original value:

--primary-color: #2563eb;

Changed value:

--primary-color: #dc2626;

Observation: The elements that use "var(--primary-color)", such as the main heading and buttons, change to red automatically.

This demonstrates that CSS variables allow multiple elements to be updated by changing a single value.

Complete HTML File ("index.html")

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Variables Design System</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>My Design System</h1>
        <p>A simple webpage using reusable CSS variables.</p>
    </header>

    <main>
        <section class="card">
            <h2>Primary Colors</h2>
            <p>Our design system uses reusable color variables.</p>
            <button>Primary Button</button>
            <button class="secondary-button">Secondary Button</button>
        </section>

        <section class="card">
            <h2>Spacing System</h2>
            <p>Small, medium, and large spacing values create a consistent layout.</p>
            <div class="spacing-box small-box">Small Spacing</div>
            <div class="spacing-box medium-box">Medium Spacing</div>
            <div class="spacing-box large-box">Large Spacing</div>
        </section>

        <section class="card">
            <h2>Typography System</h2>
            <p class="small-text">This is small text.</p>
            <p class="medium-text">This is medium text.</p>
            <p class="large-text">This is large text.</p>
        </section>
    </main>

    <footer>
        <p>Created for Assignment 5.4 — CSS Variables & Design Tokens</p>
    </footer>

</body>
</html>

Complete CSS File ("style.css")

/* Design Tokens */
:root {
    --primary-color: #2563eb;
    --secondary-color: #14b8a6;
    --background-color: #f3f4f6;
    --text-color: #1f2937;

    --spacing-small: 8px;
    --spacing-medium: 16px;
    --spacing-large: 32px;

    --font-small: 14px;
    --font-medium: 18px;
    --font-large: 32px;
}

/* General Styling */
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    padding: var(--spacing-medium);
    font-family: Arial, sans-serif;
    background-color: var(--background-color);
    color: var(--text-color);
    line-height: 1.6;
}

/* Header */
header {
    text-align: center;
    padding: var(--spacing-large);
    background-color: var(--primary-color);
    color: white;
    border-radius: var(--spacing-small);
}

h1 {
    font-size: var(--font-large);
}

h2 {
    color: var(--primary-color);
}

/* Cards */
.card {
    background-color: white;
    padding: var(--spacing-large);
    margin-top: var(--spacing-large);
    border-radius: var(--spacing-small);
    box-shadow: 0 2px 8px #d1d5db;
}

/* Buttons */
button {
    background-color: var(--primary-color);
    color: white;
    border: none;
    padding: var(--spacing-small) var(--spacing-medium);
    font-size: var(--font-medium);
    border-radius: var(--spacing-small);
    cursor: pointer;
    margin-right: var(--spacing-small);
}

.secondary-button {
    background-color: var(--secondary-color);
}

/* Spacing Examples */
.spacing-box {
    background-color: var(--secondary-color);
    color: white;
    margin-top: var(--spacing-small);
    border-radius: 4px;
}

.small-box {
    padding: var(--spacing-small);
}

.medium-box {
    padding: var(--spacing-medium);
}

.large-box {
    padding: var(--spacing-large);
}

/* Typography */
.small-text {
    font-size: var(--font-small);
}

.medium-text {
    font-size: var(--font-medium);
}

.large-text {
    font-size: var(--font-large);
}

/* Footer */
footer {
    text-align: center;
    margin-top: var(--spacing-large);
    font-size: var(--font-small);
}

Result

The webpage was created successfully using CSS variables and design tokens. Reusable variables were defined for colors, spacing, and font sizes. These variables were applied to headings, buttons, cards, and other elements.

Changing a shared variable updates all elements that use it.

Conclusion

This assignment helped me understand how CSS variables improve consistency, reusability, and maintainability in web design. I learned how to define design tokens in ":root" and use the "var()" function to apply them throughout a webpage.

Submission

1. "index.html" — Sample webpage using CSS variables.
2. "style.css" — Design-token stylesheet.
3. "Assignment-5.4.md" — Questions, answers, result, and conclusion.