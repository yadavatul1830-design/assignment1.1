Assignment 9.5 — Responsive Landing Page: Finish & Review

Q1. How do you implement tablet and mobile breakpoints?

Answer: Breakpoints are screen widths where the webpage layout changes to fit different devices. CSS media queries are used to create these layouts.

/* Tablet */
@media (max-width: 900px) {
    .features {
        grid-template-columns: repeat(2, 1fr);
    }
}

/* Mobile */
@media (max-width: 600px) {
    .features {
        grid-template-columns: 1fr;
    }
}

Q2. How do you adjust the navbar and content for small screens?

Answer: On mobile screens, navigation links can be arranged in multiple rows, and the hero content can be displayed vertically using Flexbox.

@media (max-width: 600px) {
    .navbar {
        flex-direction: column;
        text-align: center;
    }

    .hero {
        flex-direction: column;
        text-align: center;
    }
}

Q3. How do you make images and typography responsive?

Answer: Use "max-width: 100%" and "height: auto" to prevent images from stretching. Use "clamp()" to adjust font sizes according to screen width.

img {
    max-width: 100%;
    height: auto;
}

h1 {
    font-size: clamp(1.8rem, 5vw, 3rem);
}

Q4. How do you test the functionality of buttons and links?

Answer: Click every navigation link and button to check that it works correctly. Internal links should lead to the correct section, and buttons should perform their intended action.

<a href="#features">Explore Features</a>
<a href="mailto:hello@example.com">Contact Us</a>

Q5. How do you check different viewport sizes in Chrome DevTools?

Answer:

1. Open the webpage in Google Chrome.
2. Right-click and select Inspect.
3. Click the Toggle Device Toolbar icon.
4. Test mobile, tablet, and desktop screen sizes.
5. Check the alignment, images, text, and navigation.
6. Fix any problems you find.

Q6. How do you fix horizontal scrolling, overlapping, broken images, and spacing issues?

Answer: Use flexible widths, responsive images, and proper spacing. Also check that image paths are correct.

* {
    box-sizing: border-box;
}

body {
    margin: 0;
    overflow-wrap: anywhere;
}

img {
    display: block;
    max-width: 100%;
    height: auto;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: auto;
}

Q7. How do you keep HTML and CSS clean and properly formatted?

Answer: Use meaningful class names, consistent indentation, semantic HTML tags, and comments for different sections. Remove unused CSS and check that all tags and braces are properly closed.

Q8. How do you push the final changes to GitHub?

Answer: Save the updated files, open a terminal in the project folder, and run:

git add .
git commit -m "Complete responsive landing page"
git push

These commands stage the changes, create a commit, and push the updates to the configured GitHub repository.

---

Practical Implementation

This is the completed version of the landing page from Assignment 9.4.

File 1: "index.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CreativeWeb | Responsive Landing Page</title>
    <meta name="description"
          content="Explore CreativeWeb's modern, responsive digital solutions.">
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="header" id="home">
        <div class="container navbar">
            <a class="logo" href="#home">CreativeWeb</a>

            <nav aria-label="Main navigation">
                <a href="#home">Home</a>
                <a href="#features">Features</a>
                <a href="#about">About</a>
                <a href="#contact">Contact</a>
            </nav>
        </div>
    </header>

    <main>
        <section class="hero container">
            <div class="hero-content">
                <p class="eyebrow">WELCOME TO CREATIVEWEB</p>
                <h1>Build Something Amazing</h1>
                <p>
                    Discover creative digital solutions with a modern,
                    simple, and responsive design for every device.
                </p>
                <a class="button" href="#features">Explore Features</a>
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
                    Discover what makes our website useful.
                </p>

                <div class="features">
                    <article class="card">
                        <h3>Easy to Use</h3>
                        <p>Simple navigation and a user-friendly layout.</p>
                    </article>

                    <article class="card">
                        <h3>Responsive Design</h3>
                        <p>Content that adapts to different screen sizes.</p>
                    </article>

                    <article class="card">
                        <h3>Modern Style</h3>
                        <p>A clean design with consistent colors and spacing.</p>
                    </article>

                    <article class="card">
                        <h3>Creative Ideas</h3>
                        <p>Explore inspiration for your next project.</p>
                    </article>

                    <article class="card">
                        <h3>Flexible Layout</h3>
                        <p>Grid and Flexbox keep content organized.</p>
                    </article>

                    <article class="card">
                        <h3>Easy Navigation</h3>
                        <p>Quick links help users find important information.</p>
                    </article>
                </div>
            </div>
        </section>

        <section class="about container" id="about">
            <h2>About CreativeWeb</h2>
            <p>
                CreativeWeb is a sample landing page project built with
                HTML and CSS. It demonstrates responsive design,
                semantic HTML, CSS Grid, and Flexbox.
            </p>
        </section>

        <section class="contact-section" id="contact">
            <div class="container">
                <h2>Let's Connect</h2>
                <p>Have a question? Get in touch with us.</p>
                <a class="button" href="mailto:hello@example.com">
                    Contact Us
                </a>
            </div>
        </section>
    </main>

    <footer class="footer">
        <p>&copy; 2026 CreativeWeb. All rights reserved.</p>
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
    color: #243047;
    background: #ffffff;
    overflow-wrap: anywhere;
}

img {
    display: block;
    max-width: 100%;
    height: auto;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
}

/* Header and navigation */
.header {
    background: #17324d;
    color: white;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 16px;
    padding-top: 18px;
    padding-bottom: 18px;
}

.logo {
    color: white;
    font-size: 1.6rem;
    font-weight: bold;
    text-decoration: none;
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

nav a:hover,
nav a:focus-visible {
    text-decoration: underline;
}

/* Hero section */
.hero {
    display: flex;
    align-items: center;
    gap: 40px;
    padding-top: 65px;
    padding-bottom: 65px;
}

.hero-content,
.hero-image {
    flex: 1;
    min-width: 0;
}

.eyebrow {
    color: #2775b6;
    font-weight: bold;
    letter-spacing: 1px;
}

.hero h1 {
    font-size: clamp(2rem, 4vw, 3.2rem);
    line-height: 1.2;
    margin: 12px 0;
}

.hero-content > p:not(.eyebrow) {
    font-size: 1.1rem;
    max-width: 540px;
}

.hero-image img {
    width: 100%;
    border-radius: 12px;
}

/* Buttons */
.button {
    display: inline-block;
    padding: 12px 22px;
    margin-top: 12px;
    background: #2775b6;
    color: white;
    text-decoration: none;
    border-radius: 6px;
}

.button:hover,
.button:focus-visible {
    background: #1c5b8f;
}

/* Features section */
.features-section {
    padding: 55px 0;
    background: #f1f6fb;
    text-align: center;
}

.features-section h2,
.about h2,
.contact-section h2 {
    font-size: clamp(1.6rem, 3vw, 2.2rem);
}

.section-description {
    margin-bottom: 30px;
}

.features {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 24px;
}

.card {
    padding: 24px;
    background: white;
    border-radius: 10px;
    box-shadow: 0 3px 10px #dce3eb;
    text-align: left;
    min-width: 0;
}

.card h3 {
    margin-top: 0;
}

/* About section */
.about {
    padding-top: 45px;
    padding-bottom: 45px;
}

/* Contact section */
.contact-section {
    padding: 40px 0;
    text-align: center;
    background: #dbeafe;
}

/* Footer */
.footer {
    padding: 18px;
    background: #17324d;
    color: white;
    text-align: center;
}

/* Tablet breakpoint */
@media (max-width: 900px) {
    .hero {
        gap: 24px;
        padding-top: 45px;
        padding-bottom: 45px;
    }

    .features {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }
}

/* Mobile breakpoint */
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

    .hero-content > p:not(.eyebrow) {
        margin-left: auto;
        margin-right: auto;
    }

    .features {
        grid-template-columns: 1fr;
    }

    .features-section {
        padding: 35px 0;
    }

    .card {
        padding: 20px;
    }
}

Project Folder Structure

Landing-Page/
├── index.html
├── style.css
└── images/
    └── hero.jpg

Place a real image named "hero.jpg" inside the "images" folder. Otherwise, the hero image will appear broken.

Final Testing and Submission

1. Open "index.html" in Chrome.
2. Test the page at mobile, tablet, and desktop widths using Inspect → Toggle Device Toolbar.
3. Check all navigation links and buttons.
4. Fix any broken images, horizontal scrolling, overlapping, or spacing problems.
5. Take three screenshots: mobile, tablet, and desktop.
6. Push the final files to GitHub using the commands in Question 8.
7. Submit the HTML/CSS files, three screenshots, and the actual updated GitHub repository link.

Expected result: A clean, responsive landing page with a flexible navbar, responsive hero section, six feature cards, working section links, and layouts that adapt to mobile, tablet, and desktop screens.