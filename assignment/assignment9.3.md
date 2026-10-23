Assignment 9.3 — Combine Flexbox and Grid Responsively

Q1. How do you create a header and navigation bar?

Answer: A header displays the website name, while a navigation bar provides links to different sections. Flexbox helps arrange the navigation links neatly.

<header>
    <h1>My Website</h1>
    <nav class="navbar">
        <a href="#home">Home</a>
        <a href="#features">Features</a>
        <a href="#about">About</a>
    </nav>
</header>

Q2. How do you arrange text and images in a hero section?

Answer: A hero section is the main introductory area of a landing page. Flexbox can arrange the text and image side by side on larger screens.

<section class="hero" id="home">
    <div>
        <h2>Welcome to Our Website</h2>
        <p>Discover useful tools and creative ideas.</p>
    </div>
    <img src="https://placehold.co/500x300?text=Welcome"
         alt="Welcome banner">
</section>

Q3. How do you add 3–6 cards to the features section?

Answer: Feature cards display important services or benefits. Each card can contain a heading and a short description. CSS Grid arranges the cards in rows and columns.

<section class="features" id="features">
    <article class="card">
        <h3>Easy to Use</h3>
        <p>Simple and user-friendly design.</p>
    </article>
    <article class="card">
        <h3>Responsive</h3>
        <p>Works on mobile and desktop screens.</p>
    </article>
    <article class="card">
        <h3>Creative</h3>
        <p>Modern layouts for your ideas.</p>
    </article>
</section>

Q4. How do you use CSS Grid for the main section layout?

Answer: CSS Grid arranges content into rows and columns. It is useful for displaying several feature cards in an organized layout.

.features {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 20px;
}

Q5. How do you use Flexbox for the navbar, cards, or hero section?

Answer: Flexbox arranges elements in a row or column and helps align them with spacing.

.navbar {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 20px;
    flex-wrap: wrap;
}

.hero {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 30px;
}

Q6. How do you change multiple columns into a single column on mobile?

Answer: Use a media query to change the layout when the screen becomes smaller.

@media (max-width: 600px) {
    .features {
        grid-template-columns: 1fr;
    }

    .hero {
        flex-direction: column;
        text-align: center;
    }
}

Q7. How do you check spacing and alignment on mobile and desktop?

Answer: Open the webpage in Chrome and use Developer Tools' Device Mode. Check that the navbar, hero section, and cards align properly on different screen sizes. Adjust the gap, padding, and media queries wherever needed.

---

Practical Implementation

Create two files: "index.html" and "style.css".

File 1: "index.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Landing Page</title>
    <meta name="description" content="A responsive landing page built using CSS Grid and Flexbox.">
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="header" id="home">
        <h1>Creative Web</h1>

        <nav class="navbar">
            <a href="#home">Home</a>
            <a href="#features">Features</a>
            <a href="#about">About</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <main>
        <section class="hero">
            <div class="hero-text">
                <h2>Build Something Amazing</h2>
                <p>
                    Explore creative ideas with a simple, modern,
                    and responsive website design.
                </p>
                <a class="button" href="#features">Explore Features</a>
            </div>

            <img
                src="https://placehold.co/600x400?text=Creative+Web"
                alt="Creative web design illustration">
        </section>

        <section class="features-section" id="features">
            <h2>Our Features</h2>

            <div class="features">
                <article class="card">
                    <h3>Easy to Use</h3>
                    <p>Enjoy a simple and user-friendly experience.</p>
                </article>

                <article class="card">
                    <h3>Responsive Design</h3>
                    <p>Use the website comfortably on any screen.</p>
                </article>

                <article class="card">
                    <h3>Modern Layout</h3>
                    <p>Explore a clean and attractive design.</p>
                </article>

                <article class="card">
                    <h3>Fast Access</h3>
                    <p>Find important information quickly.</p>
                </article>

                <article class="card">
                    <h3>Creative Ideas</h3>
                    <p>Discover new ideas and inspiration.</p>
                </article>

                <article class="card">
                    <h3>Flexible Design</h3>
                    <p>Enjoy a layout that adjusts to your device.</p>
                </article>
            </div>
        </section>

        <section class="about" id="about">
            <h2>About Us</h2>
            <p>
                Creative Web demonstrates how Flexbox and CSS Grid
                can work together to create responsive websites.
            </p>
        </section>
    </main>

    <footer id="contact">
        <p>&copy; 2026 Creative Web. All rights reserved.</p>
    </footer>

</body>
</html>

File 2: "style.css"

/* General settings */
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
    color: #222;
    background-color: #f4f7fb;
}

img {
    max-width: 100%;
    height: auto;
    display: block;
}

/* Header and Flexbox navigation */
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 15px;
    padding: 20px 5%;
    background-color: #24476b;
    color: white;
}

.header h1 {
    margin: 0;
}

.navbar {
    display: flex;
    flex-wrap: wrap;
    gap: 18px;
}

.navbar a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

.navbar a:hover {
    text-decoration: underline;
}

/* Hero section using Flexbox */
.hero {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 35px;
    padding: 50px 5%;
    background-color: #dbeafe;
}

.hero-text {
    flex: 1;
    min-width: 0;
}

.hero-text h2 {
    font-size: clamp(2rem, 4vw, 3rem);
    line-height: 1.2;
}

.hero img {
    flex: 1;
    min-width: 0;
    width: 50%;
    border-radius: 12px;
}

.button {
    display: inline-block;
    padding: 10px 18px;
    background-color: #24476b;
    color: white;
    text-decoration: none;
    border-radius: 5px;
}

/* Features section using Grid */
.features-section {
    padding: 35px 5%;
    text-align: center;
}

.features {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 20px;
}

.card {
    padding: 22px;
    background-color: white;
    border-radius: 10px;
    box-shadow: 0 2px 6px #cccccc;
    text-align: left;
    min-width: 0;
}

/* About section */
.about {
    padding: 30px 5%;
    text-align: center;
}

/* Footer */
footer {
    padding: 15px;
    background-color: #24476b;
    color: white;
    text-align: center;
}

/* Tablet layout */
@media (max-width: 900px) {
    .features {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .hero {
        gap: 20px;
    }
}

/* Mobile layout */
@media (max-width: 600px) {
    .header {
        flex-direction: column;
        text-align: center;
    }

    .navbar {
        justify-content: center;
    }

    .hero {
        flex-direction: column;
        text-align: center;
        padding: 30px 5%;
    }

    .hero img {
        width: 100%;
    }

    .features {
        grid-template-columns: 1fr;
    }
}

Folder Structure

Responsive-Landing-Page/
├── index.html
└── style.css

Submission Checklist

1. Save the assignment as "Assignment-9.3.md".
2. Save the HTML code as "index.html".
3. Save the CSS code as "style.css" in the same folder.
4. Open "index.html" in a browser and check the layout.
5. Test the page using Chrome DevTools Device Mode.
6. Take screenshots of both the mobile and desktop layouts.
7. Submit the HTML file, CSS file, and screenshots.

Expected result: Flexbox aligns the navigation and hero content, while CSS Grid arranges six feature cards. On mobile, the hero and feature cards change to a single-column layout.