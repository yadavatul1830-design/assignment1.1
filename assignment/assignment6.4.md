Assignment 6.4 — Positioning Practice

1. Objective

To understand CSS positioning properties such as "static", "relative", "absolute", "fixed", and "sticky", and to create a webpage with a sticky navigation bar, floating contact button, positioned badge, and overlapping elements controlled by "z-index".

2. Questions and Answers

Q1. What is CSS positioning?

Answer: CSS positioning is used to control the placement of elements on a webpage. The "position" property determines how an element is positioned in relation to the normal document flow, its parent, or the viewport.

Q2. What is "position: static"?

Answer: "position: static" is the default positioning of HTML elements. Elements appear in the normal document flow, and properties such as "top", "right", "bottom", and "left" do not reposition them.

Q3. What is "position: relative"?

Answer: "position: relative" positions an element relative to its normal position. It also allows an absolutely positioned child element to use it as a positioning reference.

Q4. What is "position: absolute"?

Answer: "position: absolute" removes an element from the normal document flow and positions it relative to its nearest positioned ancestor. It is useful for placing badges, labels, and icons inside cards.

Q5. What is "position: fixed"?

Answer: "position: fixed" positions an element relative to the viewport. The element stays in the same place on the screen while the user scrolls the webpage. It is commonly used for floating contact buttons.

Q6. What is "position: sticky"?

Answer: "position: sticky" allows an element to behave normally until it reaches a specified scrolling position, after which it sticks in place. For example, a navigation bar can remain at the top using "position: sticky" and "top: 0".

Q7. What is the purpose of "z-index"?

Answer: The "z-index" property controls the stacking order of overlapping positioned elements. An element with a higher "z-index" generally appears in front of an element with a lower value within the relevant stacking context.

Q8. Why do we use "position: relative" on a card?

Answer: We use "position: relative" on a card to make it the positioning reference for absolutely positioned child elements, such as a badge in the top-right corner.

Q9. What is a floating action button?

Answer: A floating action button is a button that remains visible at a fixed position on the screen, even when the page is scrolled. It can be used for contact, help, or quick actions.

3. HTML Code

Create a file named "index.html" and paste the following code.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 6.4 - Positioning Practice</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="hero" id="home">
        <h1>CSS Positioning Practice</h1>
        <p>Learn how CSS positions elements on a webpage.</p>
    </header>

    <nav class="navbar">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
    </nav>

    <main class="container">

        <section id="about" class="section">
            <h2>About CSS Positioning</h2>
            <p>
                CSS positioning helps us place elements at specific locations
                on a webpage. Different positioning values provide different
                layout behaviors.
            </p>
        </section>

        <section id="services" class="section">
            <h2>Our Services</h2>
            <p>
                We provide web design, website development, and responsive
                layout solutions using HTML and CSS.
            </p>

            <div class="card">
                <span class="badge">Popular</span>
                <h3>Web Development</h3>
                <p>
                    Learn to create attractive and responsive websites
                    using modern web technologies.
                </p>
                <a class="card-link" href="#contact">Learn More</a>
            </div>
        </section>

        <section class="section">
            <h2>Why Positioning Matters</h2>
            <p>
                Positioning is useful for sticky navigation bars, floating
                buttons, notification badges, and layered webpage elements.
            </p>
            <p>
                Scroll down to see how the sticky navigation bar and
                floating contact button behave.
            </p>
        </section>

        <section id="contact" class="section">
            <h2>Contact Us</h2>
            <p>Email: support@example.com</p>
            <p>Phone: +91 98765 43210</p>
            <p>
                The floating Help button stays visible as you scroll
                through the page.
            </p>
        </section>

    </main>

    <footer>
        <p>Assignment 6.4 | CSS Positioning Practice</p>
    </footer>

    <a class="floating-button" href="#contact" aria-label="Contact or get help">
        Help
    </a>

</body>
</html>

4. CSS Code

Create a file named "style.css" in the same folder and paste the following code.

* {
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    scroll-padding-top: 80px;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #1e293b;
    background-color: #f1f5f9;
}

.hero {
    padding: 35px 20px;
    text-align: center;
    color: white;
    background-color: #1d4ed8;
}

.hero h1 {
    margin-top: 0;
}

.navbar {
    position: sticky;
    top: 0;
    z-index: 1000;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 25px;
    padding: 15px;
    background-color: #0f172a;
}

.navbar a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

.navbar a:hover {
    color: #93c5fd;
}

.container {
    width: 100%;
    max-width: 900px;
    margin: 0 auto;
    padding: 20px;
}

.section {
    min-height: 250px;
    margin-bottom: 25px;
    padding: 25px;
    background-color: white;
    border: 1px solid #cbd5e1;
    border-radius: 10px;
}

.card {
    position: relative;
    margin-top: 25px;
    padding: 30px 20px 20px;
    border: 2px solid #2563eb;
    border-radius: 10px;
    background-color: #eff6ff;
}

.badge {
    position: absolute;
    top: 10px;
    right: 10px;
    z-index: 2;
    padding: 5px 10px;
    color: white;
    background-color: #dc2626;
    border-radius: 15px;
    font-size: 12px;
    font-weight: bold;
}

.card-link {
    display: inline-block;
    padding: 8px 14px;
    color: white;
    background-color: #2563eb;
    text-decoration: none;
    border-radius: 5px;
}

.card-link:hover {
    background-color: #1e40af;
}

.floating-button {
    position: fixed;
    right: 20px;
    bottom: 20px;
    z-index: 1100;
    display: inline-block;
    padding: 14px 20px;
    color: white;
    background-color: #16a34a;
    border-radius: 30px;
    text-decoration: none;
    font-weight: bold;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
}

.floating-button:hover {
    background-color: #15803d;
}

footer {
    padding: 20px;
    text-align: center;
    color: white;
    background-color: #0f172a;
}

@media (max-width: 600px) {
    .navbar {
        gap: 15px;
    }

    .container {
        padding: 12px;
    }

    .section {
        padding: 18px;
    }

    .floating-button {
        right: 12px;
        bottom: 12px;
    }
}

5. Explanation of Important CSS Properties

Property| Purpose
"position: sticky"| Keeps the navigation bar at the top while scrolling.
"position: fixed"| Keeps the Help button at the bottom-right of the screen.
"position: relative"| Establishes the card as a positioning reference.
"position: absolute"| Places the Popular badge inside the card.
"z-index: 1000"| Places the navigation bar above ordinary page content.
"z-index: 1100"| Places the floating button above the navigation bar in overlapping areas.
"top: 0"| Makes the sticky navbar stick to the top.
"bottom: 20px"| Sets the floating button's distance from the bottom of the viewport.

6. Result

The webpage successfully demonstrates CSS positioning. The navigation bar sticks to the top while scrolling, the Help button remains fixed at the bottom-right, and the Popular badge is positioned inside the card using absolute positioning. The "z-index" property controls the stacking order of overlapping elements.

7. Conclusion

In this assignment, I learned how to use CSS positioning properties, including relative, absolute, fixed, and sticky. I also learned how to position elements inside a parent container and control overlapping elements using "z-index".

8. Submission Checklist

- [ ] "Assignment-6.4.md"
- [ ] "index.html"
- [ ] "style.css"
- [ ] Screenshot showing the sticky navigation bar.
- [ ] Screenshot showing the floating Help button.
- [ ] Screenshot showing the Popular badge inside the card.