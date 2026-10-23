Assignment 9.4 — Responsive Landing Page: Build

Q1. How do you identify colors, typography, images, and layout from a reference design?

Answer: First, observe the reference design carefully.

- Colors: Identify the background, text, and button colors.
- Typography: Identify the font style, size, and weight.
- Images: Check the images used in the hero section and feature cards.
- Layout: Observe the position of the navbar, headings, buttons, and cards.

These details help create a webpage similar to the reference design.

Q2. How do you create "index.html", "style.css", and an images folder?

Answer: Create a project folder named "Landing-Page". Inside it, create an HTML file, a CSS file, and an "images" folder.

Landing-Page/
├── index.html
├── style.css
└── images/
    └── hero.jpg

The HTML file contains the webpage structure, the CSS file controls its appearance, and the images folder stores image files.

Q3. How do you create semantic sections in HTML?

Answer: Semantic HTML tags describe the purpose of each section.

- "<header>" defines the page header.
- "<nav>" contains navigation links.
- "<main>" contains the main content.
- "<section>" groups related content.
- "<footer>" contains footer information.

These tags make the code easier to understand and maintain.

Q4. How do you build the navbar, hero section, buttons, and feature cards?

Answer: Use HTML elements to create each part of the landing page. The navbar contains links, the hero section introduces the website, buttons encourage users to take action, and feature cards display benefits.

<nav>
    <a href="#home">Home</a>
    <a href="#features">Features</a>
    <a href="#about">About</a>
</nav>

<section class="hero" id="home">
    <h2>Build Your Future</h2>
    <p>Discover simple and creative digital solutions.</p>
    <a class="button" href="#features">Get Started</a>
</section>

Q5. How do you implement the desktop layout in CSS?

Answer: Use CSS to set the colors, font sizes, spacing, and alignment. For desktop layouts, Flexbox can align items in a row, while Grid can arrange feature cards in columns.

.hero {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 30px;
    padding: 60px;
}

.features {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 20px;
}

Q6. How do you use CSS Grid and Flexbox appropriately?

Answer: CSS Grid is useful for two-dimensional layouts, such as feature cards arranged in rows and columns. Flexbox is useful for one-dimensional layouts, such as navigation links, buttons, and hero content.

Using both makes the webpage organized and easier to style.

Q7. How do you complete the base styling and spacing?

Answer: Apply consistent colors, fonts, margins, padding, and borders. Use "box-sizing: border-box" to make element sizing easier to control and "max-width: 100%" to prevent images from exceeding their containers.

* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

img {
    max-width: 100%;
    height: auto;
    display: block;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: auto;
}

Q8. How do you push the landing page code to GitHub?

Answer: GitHub stores the project online and provides a link for sharing the code.

1. Create a GitHub account or sign in.
2. Create a new repository named "Landing-Page".
3. Open the project folder in a terminal.
4. Run the following commands:

git init
git add .
git commit -m "Create initial landing page"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/Landing-Page.git
git push -u origin main

Replace "YOUR-USERNAME" with your actual GitHub username. The remote URL must match the repository you created.

---

Practical Implementation

Create the following two files and an images folder.

File 1: "index.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Creative Landing Page</title>
    <meta name="description" content="Discover creative digital solutions and useful features.">
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="header">
        <div class="container navbar">
            <h1 class="logo">CreativeWeb</h1>

            <nav aria-label="Main navigation">
                <a href="#home">Home</a>
                <a href="#features">Features</a>
                <a href="#about">About</a>
                <a href="#contact">Contact</a>
            </nav>
        </div>
    </header>

    <main>
        <section class="hero container" id="home">
            <div class="hero-content">
                <p class="eyebrow">WELCOME TO CREATIVEWEB</p>
                <h2>Build Something Amazing</h2>
                <p>
                    Explore creative digital solutions designed to help
                    you learn, create, and grow.
                </p>
                <a class="button" href="#features">Get Started</a>
            </div>

            <div class="hero-image">
                <img src="images/hero.jpg"
                     alt="Creative workspace with a laptop">
            </div>
        </section>

        <section class="features-section" id="features">
            <div class="container">
                <h2>Our Features</h2>
                <p class="section-description">
                    Everything you need to get started.
                </p>

                <div class="features-grid">
                    <article class="feature-card">
                        <h3>Easy to Use</h3>
                        <p>A simple design that is easy to understand.</p>
                    </article>

                    <article class="feature-card">
                        <h3>Modern Design</h3>
                        <p>A clean layout with attractive styling.</p>
                    </article>

                    <article class="feature-card">
                        <h3>Flexible Layout</h3>
                        <p>Content arranged neatly for different screens.</p>
                    </article>
                </div>
            </div>
        </section>

        <section class="about container" id="about">
            <h2>About CreativeWeb</h2>
            <p>
                CreativeWeb is a sample landing page project built using
                HTML and CSS. It demonstrates semantic HTML, Flexbox,
                Grid, and basic desktop styling.
            </p>
        </section>
    </main>

    <footer id="contact">
        <p>&copy; 2026 CreativeWeb. All rights reserved.</p>
    </footer>

</body>
</html>

File 2: "style.css"

/* Basic settings */
* {
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #243047;
    background-color: #ffffff;
}

img {
    max-width: 100%;
    height: auto;
    display: block;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
}

/* Navigation */
.header {
    background-color: #17324d;
    color: white;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 15px;
    padding-top: 18px;
    padding-bottom: 18px;
}

.logo {
    margin: 0;
    font-size: 1.6rem;
}

nav {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
}

nav a {
    color: white;
    text-decoration: none;
}

nav a:hover {
    text-decoration: underline;
}

/* Hero section */
.hero {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 40px;
    padding-top: 70px;
    padding-bottom: 70px;
}

.hero-content {
    flex: 1;
    min-width: 0;
}

.eyebrow {
    color: #2775b6;
    font-weight: bold;
    letter-spacing: 1px;
}

.hero h2 {
    font-size: 3rem;
    line-height: 1.2;
    margin: 10px 0;
}

.hero-content > p:not(.eyebrow) {
    font-size: 1.1rem;
    max-width: 520px;
}

.hero-image {
    flex: 1;
    min-width: 0;
}

.hero-image img {
    width: 100%;
    border-radius: 12px;
    object-fit: cover;
}

.button {
    display: inline-block;
    padding: 12px 22px;
    background-color: #2775b6;
    color: white;
    text-decoration: none;
    border-radius: 6px;
    margin-top: 12px;
}

.button:hover {
    background-color: #1c5b8f;
}

/* Feature cards using Grid */
.features-section {
    background-color: #f1f6fb;
    padding: 55px 0;
    text-align: center;
}

.features-section h2,
.about h2 {
    font-size: 2rem;
}

.section-description {
    margin-bottom: 30px;
}

.features-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 24px;
}

.feature-card {
    background-color: white;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 3px 10px #dce3eb;
    text-align: left;
    min-width: 0;
}

/* About section */
.about {
    padding-top: 45px;
    padding-bottom: 45px;
}

/* Footer */
footer {
    background-color: #17324d;
    color: white;
    text-align: center;
    padding: 18px;
}

/* Tablet layout */
@media (max-width: 900px) {
    .hero {
        gap: 25px;
        padding-top: 45px;
        padding-bottom: 45px;
    }

    .hero h2 {
        font-size: 2.3rem;
    }

    .features-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }
}

/* Mobile layout */
@media (max-width: 600px) {
    .navbar {
        flex-direction: column;
        text-align: center;
    }

    nav {
        justify-content: center;
        gap: 12px;
    }

    .hero {
        flex-direction: column;
        text-align: center;
    }

    .hero h2 {
        font-size: 2rem;
    }

    .hero-content > p:not(.eyebrow) {
        margin-left: auto;
        margin-right: auto;
    }

    .features-grid {
        grid-template-columns: 1fr;
    }

    .features-section {
        padding: 35px 0;
    }
}

Folder Structure

Landing-Page/
├── index.html
├── style.css
└── images/
    └── hero.jpg

Important: Place a real image named "hero.jpg" inside the "images" folder. The HTML references that exact path.

Submission Checklist

1. Save the assignment as "Assignment-9.4.md".
2. Create "index.html", "style.css", and the "images" folder.
3. Open the webpage in a browser and check the desktop layout.
4. Take a screenshot of the initial landing page.
5. Push the project files to your GitHub repository.
6. Submit the HTML/CSS files, screenshot, and your actual GitHub repository link.