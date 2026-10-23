Assignment 7.1 — Responsive Navigation Bar

Objective

To create a responsive horizontal navigation bar using CSS Flexbox, including a logo, navigation links, and a button. The layout should remain usable on different screen widths.

Q1. What is a navigation bar?

Answer: A navigation bar is a section of a website that contains links to important pages, such as Home, About, Services, and Contact. It helps users navigate through a website easily.

Q2. What is CSS Flexbox?

Answer: CSS Flexbox is a layout system used to arrange elements in a row or column. It helps distribute space and align items within a container.

Q3. What is the purpose of "display: flex"?

Answer: The "display: flex" property turns an element into a flex container. Its direct children become flex items and can be arranged using Flexbox properties.

Q4. What does "justify-content" do?

Answer: The "justify-content" property controls how flex items are distributed along the main axis. For example, "justify-content: space-between" places space between items and pushes the first and last items toward opposite ends.

Q5. What does "align-items" do?

Answer: The "align-items" property aligns flex items along the cross axis. For a horizontal navigation bar, "align-items: center" vertically aligns the logo, links, and button.

Q6. How can we style navigation links?

Answer: Navigation links can be styled using CSS properties such as "color", "text-decoration", "padding", "font-size", and "font-weight". The ":hover" pseudo-class can change their appearance when the pointer moves over them.

Q7. What is responsive web design?

Answer: Responsive web design allows a webpage to adapt to different screen sizes, including mobile phones, tablets, and desktop computers. CSS media queries can modify the layout when the screen width changes.

Q8. Why should we inspect the navigation bar at different browser widths?

Answer: Inspecting the navigation bar at different widths helps identify layout problems, such as overlapping links, overflowing content, or buttons moving outside the screen. It also helps ensure a good user experience on mobile devices.

2. HTML Code

Create a file named "index.html" and paste the following code.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 7.1 - Responsive Navigation Bar</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="site-header">
        <nav class="navbar">
            <a href="#home" class="logo">FlexSite</a>

            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>

            <a href="#contact" class="nav-button">Get Started</a>
        </nav>
    </header>

    <main>
        <section id="home" class="hero">
            <h1>Welcome to FlexSite</h1>
            <p>A simple responsive navigation bar built with CSS Flexbox.</p>
            <a href="#about" class="hero-button">Explore More</a>
        </section>

        <section id="about" class="content-section">
            <h2>About Us</h2>
            <p>
                We create simple and responsive website layouts using
                HTML and CSS.
            </p>
        </section>

        <section id="services" class="content-section">
            <h2>Our Services</h2>
            <p>
                Our services include web design, frontend development,
                and responsive website layouts.
            </p>
        </section>

        <section id="contact" class="content-section">
            <h2>Contact Us</h2>
            <p>Email: contact@example.com</p>
        </section>
    </main>

    <footer class="site-footer">
        <p>Assignment 7.1 | Responsive Navigation Bar</p>
    </footer>

</body>
</html>

3. CSS Code

Create a file named "style.css" in the same folder and paste this code.

* {
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    scroll-padding-top: 90px;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    color: #1e293b;
    background-color: #f8fafc;
}

.site-header {
    background-color: #0f172a;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 20px;
    max-width: 1200px;
    margin: 0 auto;
    padding: 18px 24px;
}

.logo {
    color: #60a5fa;
    font-size: 25px;
    font-weight: bold;
    text-decoration: none;
}

.nav-links {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    gap: 25px;
    margin: 0;
    padding: 0;
    list-style: none;
}

.nav-links a {
    color: white;
    font-size: 15px;
    text-decoration: none;
    transition: color 0.2s ease;
}

.nav-links a:hover {
    color: #60a5fa;
}

.nav-button,
.hero-button {
    display: inline-block;
    padding: 10px 18px;
    color: white;
    background-color: #2563eb;
    border-radius: 7px;
    font-weight: bold;
    text-decoration: none;
}

.nav-button:hover,
.hero-button:hover {
    background-color: #1d4ed8;
}

.hero {
    padding: 90px 20px;
    text-align: center;
    background: linear-gradient(135deg, #dbeafe, #eff6ff);
}

.hero h1 {
    margin-top: 0;
    font-size: 38px;
}

.hero p {
    margin-bottom: 25px;
    line-height: 1.7;
}

.content-section {
    max-width: 900px;
    min-height: 180px;
    margin: 25px auto;
    padding: 30px 24px;
    background-color: white;
    border: 1px solid #e2e8f0;
    border-radius: 10px;
}

.content-section h2 {
    color: #1d4ed8;
}

.site-footer {
    padding: 20px;
    color: white;
    background-color: #0f172a;
    text-align: center;
}

@media (max-width: 650px) {
    .navbar {
        flex-direction: column;
        justify-content: center;
        gap: 18px;
        padding: 20px 14px;
    }

    .nav-links {
        gap: 16px;
    }

    .nav-links a {
        font-size: 14px;
    }

    .hero {
        padding: 60px 16px;
    }

    .hero h1 {
        font-size: 29px;
    }

    .content-section {
        margin: 16px 12px;
        padding: 22px 18px;
    }
}

4. Explanation of Important CSS Properties

Property| Purpose
"display: flex"| Arranges navigation items using Flexbox.
"justify-content: space-between"| Distributes space between the logo, links, and button.
"align-items: center"| Vertically aligns items in the navigation bar.
"flex-wrap: wrap"| Allows items to move to another line when necessary.
"gap"| Adds spacing between flex items.
"flex-direction: column"| Stacks navbar items vertically on smaller screens.
"@media"| Applies responsive styles when the screen width is 650px or less.

5. Result

The responsive navigation bar was successfully created using HTML and CSS Flexbox. It contains a logo, navigation links, and a Get Started button. The layout uses "justify-content" and "align-items" for spacing and alignment and adapts to smaller screens using a CSS media query.

6. Conclusion

In this assignment, I learned how to create a horizontal navigation bar using CSS Flexbox. I understood how to use "display: flex", "justify-content", "align-items", "gap", and media queries to build a responsive layout that works on different screen sizes.

7. Submission Checklist

- [ ] "Assignment-7.1.md"
- [ ] "index.html"
- [ ] "style.css"
- [ ] Screenshot of the desktop navigation bar.
- [ ] Screenshot of the navigation bar in mobile view.