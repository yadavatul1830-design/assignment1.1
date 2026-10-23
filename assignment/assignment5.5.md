Assignment 5.5 — CSS Fundamentals Mini-Project

Objective

To style the multi-page college club website created in Week 4 using external CSS, consistent colors, typography, CSS selectors, and reusable variables.

Question 1: Use external CSS.

Answer:

An external CSS file is used to separate the styling from HTML content. I created a file named "style.css" and linked it to all HTML pages using the following code inside the "<head>" section:

<link rel="stylesheet" href="style.css">

This makes the website easier to maintain and update.

Question 2: Choose a consistent color palette and typography.

Answer:

I selected a blue, white, and light-gray color palette to give the website a clean and professional appearance. Arial is used as the main font because it is simple and readable.

The CSS variables define reusable colors, spacing, and font sizes in the ":root" selector.

Question 3: Style navigation, headings, paragraphs, and buttons.

Answer:

The navigation bar uses a dark-blue background with white links. Headings use the primary color, paragraphs have readable line spacing, and buttons use consistent colors, padding, and rounded corners.

Question 4: Make forms and tables readable.

Answer:

Forms are styled with clear labels, properly sized input fields, and consistent spacing. Tables use borders, padding, alternating row backgrounds, and a colored header to improve readability.

Question 5: Use CSS selectors and variables.

Answer:

The website uses the following CSS selectors:

- Element selectors: "body", "h1", and "p"
- Class selectors: ".card", ".btn", and ".form-group"
- ID selectors: "#home" and "#contact"
- Universal selector: "*"
- Grouping selector: "h1, h2, h3"

CSS variables such as "--primary-color", "--spacing-medium", and "--font-size" help maintain consistent styling across all pages.

Question 6: Debug styling issues using DevTools.

Answer:

I opened the website in Google Chrome, right-clicked the page, and selected Inspect. In the Elements tab, I selected HTML elements and checked their CSS properties in the Styles panel. I temporarily modified CSS values to test the design and refreshed the page to restore the saved styling.

Question 7: Keep CSS clean and reusable.

Answer:

I organized the stylesheet into sections for global styles, navigation, buttons, cards, forms, tables, and footer styling. I reused CSS variables and classes to avoid repeating the same styles.

Complete HTML File 1: "index.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>College Club - Home</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="site-header">
        <h1>College Club</h1>
        <p>Learn, Connect, and Grow Together</p>
    </header>

    <nav class="navbar">
        <a href="index.html">Home</a>
        <a href="events.html">Events</a>
        <a href="contact.html">Contact</a>
    </nav>

    <main class="container" id="home">
        <section class="card">
            <h2>Welcome to Our College Club</h2>
            <p>
                Our college club helps students develop skills,
                explore interests, participate in activities,
                and build teamwork.
            </p>
            <a class="btn" href="events.html">Explore Events</a>
        </section>

        <section class="card">
            <h2>Our Activities</h2>
            <p>We organize workshops, competitions, and student events.</p>
            <p>Students can learn new skills and collaborate with others.</p>
        </section>
    </main>

    <footer class="site-footer">
        <p>College Club Website | Created for CSS Fundamentals Mini-Project</p>
    </footer>

</body>
</html>

Complete HTML File 2: "events.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>College Club - Events</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="site-header">
        <h1>College Club Events</h1>
        <p>Discover Our Activities</p>
    </header>

    <nav class="navbar">
        <a href="index.html">Home</a>
        <a href="events.html">Events</a>
        <a href="contact.html">Contact</a>
    </nav>

    <main class="container">
        <section class="card">
            <h2>Upcoming Activities</h2>

            <table>
                <thead>
                    <tr>
                        <th>Event Name</th>
                        <th>Activity</th>
                        <th>Mode</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Web Design Workshop</td>
                        <td>Learn HTML and CSS</td>
                        <td>Practical</td>
                    </tr>
                    <tr>
                        <td>Quiz Competition</td>
                        <td>Test Your Knowledge</td>
                        <td>Competition</td>
                    </tr>
                    <tr>
                        <td>Team Building</td>
                        <td>Improve Collaboration</td>
                        <td>Group Activity</td>
                    </tr>
                </tbody>
            </table>
        </section>

        <section class="card">
            <h2>Join an Activity</h2>
            <p>Visit our contact page to express your interest in joining the club.</p>
            <a class="btn" href="contact.html">Contact Us</a>
        </section>
    </main>

    <footer class="site-footer">
        <p>College Club Website | Events Page</p>
    </footer>

</body>
</html>

Complete HTML File 3: "contact.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>College Club - Contact</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="site-header">
        <h1>Contact Our Club</h1>
        <p>We Would Love to Hear From You</p>
    </header>

    <nav class="navbar">
        <a href="index.html">Home</a>
        <a href="events.html">Events</a>
        <a href="contact.html">Contact</a>
    </nav>

    <main class="container" id="contact">
        <section class="card">
            <h2>Contact Form</h2>

            <form action="#" method="post">
                <div class="form-group">
                    <label for="name">Full Name</label>
                    <input type="text" id="name" name="name"
                           placeholder="Enter your name" required>
                </div>

                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" name="email"
                           placeholder="Enter your email" required>
                </div>

                <div class="form-group">
                    <label for="subject">Subject</label>
                    <input type="text" id="subject" name="subject"
                           placeholder="Enter your subject" required>
                </div>

                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea id="message" name="message" rows="5"
                              placeholder="Write your message" required></textarea>
                </div>

                <button class="btn" type="submit">Submit</button>
            </form>
        </section>
    </main>

    <footer class="site-footer">
        <p>College Club Website | Contact Page</p>
    </footer>

</body>
</html>

Complete CSS File: "style.css"

/* 1. Design Tokens */
:root {
    --primary-color: #1e3a8a;
    --secondary-color: #2563eb;
    --accent-color: #14b8a6;
    --background-color: #f3f6fb;
    --surface-color: #ffffff;
    --text-color: #1f2937;
    --border-color: #d1d5db;

    --spacing-small: 8px;
    --spacing-medium: 16px;
    --spacing-large: 32px;

    --font-size-small: 14px;
    --font-size-medium: 16px;
    --font-size-large: 28px;
}

/* 2. Global Styles */
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    background-color: var(--background-color);
    color: var(--text-color);
    font-size: var(--font-size-medium);
    line-height: 1.6;
}

h1, h2, h3 {
    color: var(--primary-color);
    line-height: 1.3;
}

p {
    margin-bottom: var(--spacing-medium);
}

/* 3. Header */
.site-header {
    background-color: var(--primary-color);
    color: white;
    text-align: center;
    padding: var(--spacing-large) var(--spacing-medium);
}

.site-header h1 {
    color: white;
    font-size: var(--font-size-large);
    margin: 0;
}

.site-header p {
    margin-bottom: 0;
}

/* 4. Navigation */
.navbar {
    background-color: var(--secondary-color);
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: var(--spacing-small);
    padding: var(--spacing-medium);
}

.navbar a {
    color: white;
    text-decoration: none;
    font-weight: bold;
    padding: var(--spacing-small) var(--spacing-medium);
    border-radius: 5px;
}

.navbar a:hover {
    background-color: var(--primary-color);
}

/* 5. Main Container */
.container {
    width: 90%;
    max-width: 1000px;
    margin: var(--spacing-large) auto;
}

/* 6. Cards */
.card {
    background-color: var(--surface-color);
    padding: var(--spacing-large);
    margin-bottom: var(--spacing-large);
    border-radius: 10px;
    box-shadow: 0 3px 10px rgba(0, 0, 0, 0.08);
}

.card h2 {
    margin-top: 0;
}

/* 7. Buttons */
.btn {
    display: inline-block;
    background-color: var(--accent-color);
    color: #083344;
    padding: var(--spacing-small) var(--spacing-medium);
    border: none;
    border-radius: 5px;
    text-decoration: none;
    font-size: var(--font-size-medium);
    font-weight: bold;
    cursor: pointer;
}

.btn:hover {
    background-color: #0d9488;
    color: white;
}

/* 8. Tables */
table {
    width: 100%;
    border-collapse: collapse;
    margin-top: var(--spacing-medium);
    background-color: var(--surface-color);
}

th, td {
    border: 1px solid var(--border-color);
    padding: var(--spacing-medium);
    text-align: left;
}

th {
    background-color: var(--primary-color);
    color: white;
}

tbody tr:nth-child(even) {
    background-color: #eff6ff;
}

/* 9. Forms */
.form-group {
    margin-bottom: var(--spacing-medium);
}

label {
    display: block;
    margin-bottom: var(--spacing-small);
    font-weight: bold;
}

input, textarea {
    width: 100%;
    padding: var(--spacing-medium);
    border: 1px solid var(--border-color);
    border-radius: 5px;
    font: inherit;
    background-color: white;
}

input:focus, textarea:focus {
    outline: 2px solid var(--secondary-color);
    border-color: var(--secondary-color);
}

/* 10. Footer */
.site-footer {
    text-align: center;
    padding: var(--spacing-medium);
    background-color: var(--primary-color);
    color: white;
    font-size: var(--font-size-small);
}

.site-footer p {
    margin: 0;
}

/* 11. Responsive Design */
@media (max-width: 600px) {
    .container {
        width: 95%;
    }

    .card {
        padding: var(--spacing-medium);
    }

    .navbar {
        flex-direction: column;
        align-items: center;
    }

    table {
        font-size: var(--font-size-small);
    }

    th, td {
        padding: var(--spacing-small);
    }
}

Design Choices (4–5 Lines)

1. I selected blue, white, and light gray to create a clean and professional college website.
2. Arial typography was chosen because it is simple and easy to read.
3. CSS variables provide consistent colors, spacing, and font sizes throughout all pages.
4. Cards, buttons, navigation links, forms, and tables were styled to improve usability and readability.
5. Responsive CSS helps the website adjust to smaller screens, while Chrome DevTools helps identify and debug styling issues.

Result

The multi-page college club website was styled successfully using an external CSS file. All pages share consistent colors, typography, navigation, buttons, forms, and reusable design rules.

Conclusion

This project helped me understand how to apply CSS fundamentals to a multi-page website. I learned to use external stylesheets, selectors, CSS variables, responsive design, and Chrome DevTools to build a consistent and maintainable website.

Submission

1. "index.html" — Home page.
2. "events.html" — Events page with a table.
3. "contact.html" — Contact page with a form.
4. "style.css" — Shared external stylesheet.
5. "Assignment-5.5.md" — Questions, answers, design choices, result, and conclusion.