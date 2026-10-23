Assignment 7.4 — Modern Landing Page Header

Objective

To design a modern and responsive landing page header and hero section using HTML and CSS Flexbox. The webpage includes a logo, navigation links, a call-to-action (CTA) button, a heading, a paragraph, an image, and a footer.

Q1. What is a landing page?

Answer: A landing page is a webpage designed to introduce a product, service, or idea and encourage visitors to take a specific action, such as signing up, learning more, or contacting a business.

Q2. What is a hero section?

Answer: A hero section is the main introductory area of a webpage. It usually contains a prominent heading, a short description, a call-to-action button, and sometimes an image or illustration.

Q3. What is a CTA button?

Answer: CTA stands for Call to Action. It is a button or link that encourages users to perform a specific action, such as getting started, signing up, or exploring a service.

Q4. How is Flexbox used in a landing page?

Answer: Flexbox is used to arrange elements in a flexible row or column. In this project, it places the hero text and image side-by-side on larger screens and stacks them vertically on smaller screens.

Q5. What is the purpose of "align-items"?

Answer: The "align-items" property aligns flex items along the cross axis. The value "center" vertically aligns the hero text and image when the layout is arranged in a row.

Q6. What is the purpose of "justify-content"?

Answer: The "justify-content" property controls the distribution of space between flex items along the main axis. For example, "space-between" places items toward opposite ends of a container.

Q7. Why are media queries used?

Answer: Media queries apply different CSS rules at different screen widths. They help make a landing page responsive so that it works properly on desktop computers, tablets, and mobile phones.

Q8. Why is a footer important?

Answer: A footer provides additional information, such as copyright details, contact information, and useful links. It appears at the bottom of the webpage and helps users find important information.

2. HTML Code

Create a file named "index.html" and paste the following code.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 7.4 - Modern Landing Page</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="site-header">
        <nav class="navbar">
            <a href="#home" class="logo">NovaTech</a>

            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#features">Features</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>

            <a href="#contact" class="header-button">Get Started</a>
        </nav>
    </header>

    <main>
        <section class="hero" id="home">
            <div class="hero-content">
                <span class="hero-label">WELCOME TO NOVATECH</span>

                <h1>Build Something Amazing with Technology</h1>

                <p>
                    Discover modern digital solutions designed to make
                    your work easier, improve productivity, and turn
                    your ideas into reality.
                </p>

                <div class="hero-actions">
                    <a href="#contact" class="primary-button">
                        Get Started
                    </a>

                    <a href="#features" class="secondary-button">
                        Learn More
                    </a>
                </div>
            </div>

            <div class="hero-image">
                <img
                    src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?w=900&auto=format&fit=crop"
                    alt="Modern workspace with a computer and laptop"
                >
            </div>
        </section>

        <section class="features-section" id="features">
            <h2>Why Choose Us?</h2>

            <div class="features-container">
                <article class="feature-card">
                    <h3>Modern Design</h3>
                    <p>
                        Clean and attractive layouts for a better
                        user experience.
                    </p>
                </article>

                <article class="feature-card">
                    <h3>Responsive Layout</h3>
                    <p>
                        A flexible design that adapts to different
                        screen sizes.
                    </p>
                </article>

                <article class="feature-card">
                    <h3>Easy to Use</h3>
                    <p>
                        Simple interfaces that help users find
                        information quickly.
                    </p>
                </article>
            </div>
        </section>

        <section class="about-section" id="about">
            <h2>About NovaTech</h2>
            <p>
                NovaTech is a sample brand created to demonstrate
                modern landing page design using HTML and CSS.
            </p>
        </section>

        <section class="contact-section" id="contact">
            <h2>Ready to Get Started?</h2>
            <p>Explore new possibilities with a modern web experience.</p>
            <a href="mailto:contact@example.com" class="primary-button">
                Contact Us
            </a>
        </section>
    </main>

    <footer class="site-footer">
        <p>© 2026 NovaTech. All rights reserved.</p>
        <a href="#home">Back to Top ↑</a>
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
    scroll-padding-top: 85px;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    color: #172033;
    background-color: #ffffff;
    line-height: 1.6;
}

a {
    text-decoration: none;
}

/* Header and navigation */
.site-header {
    position: sticky;
    top: 0;
    z-index: 1000;
    background-color: #ffffff;
    border-bottom: 1px solid #e2e8f0;
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
    color: #4f46e5;
    font-size: 26px;
    font-weight: bold;
}

.nav-links {
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    gap: 24px;
    margin: 0;
    padding: 0;
    list-style: none;
}

.nav-links a {
    color: #334155;
    font-size: 15px;
}

.nav-links a:hover {
    color: #4f46e5;
}

.header-button,
.primary-button {
    display: inline-block;
    padding: 12px 20px;
    color: white;
    background-color: #4f46e5;
    border-radius: 8px;
    font-weight: bold;
}

.header-button:hover,
.primary-button:hover {
    background-color: #3730a3;
}

/* Hero section */
.hero {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 45px;
    max-width: 1200px;
    min-height: 560px;
    margin: 0 auto;
    padding: 70px 24px;
    background-color: #ffffff;
}

.hero-content {
    flex: 1 1 50%;
    min-width: 0;
}

.hero-label {
    display: inline-block;
    margin-bottom: 15px;
    color: #4f46e5;
    font-size: 13px;
    font-weight: bold;
    letter-spacing: 1.5px;
}

.hero-content h1 {
    margin: 0 0 20px;
    color: #111827;
    font-size: clamp(32px, 4vw, 52px);
    line-height: 1.15;
}

.hero-content p {
    max-width: 520px;
    margin: 0 0 28px;
    color: #64748b;
    font-size: 17px;
}

.hero-actions {
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    gap: 15px;
}

.secondary-button {
    display: inline-block;
    padding: 11px 19px;
    color: #4f46e5;
    border: 1px solid #4f46e5;
    border-radius: 8px;
    font-weight: bold;
}

.secondary-button:hover {
    background-color: #eef2ff;
}

.hero-image {
    flex: 1 1 50%;
    min-width: 0;
}

.hero-image img {
    display: block;
    width: 100%;
    max-width: 550px;
    height: 380px;
    margin: 0 auto;
    object-fit: cover;
    border-radius: 18px;
    box-shadow: 0 15px 35px rgba(15, 23, 42, 0.12);
}

/* Features section */
.features-section {
    padding: 65px 24px;
    background-color: #f8fafc;
    text-align: center;
}

.features-section h2,
.about-section h2,
.contact-section h2 {
    margin-top: 0;
    font-size: 32px;
}

.features-container {
    display: flex;
    justify-content: center;
    align-items: stretch;
    flex-wrap: wrap;
    gap: 24px;
    max-width: 1100px;
    margin: 30px auto 0;
}

.feature-card {
    flex: 1 1 240px;
    max-width: 340px;
    padding: 25px;
    background-color: white;
    border: 1px solid #e2e8f0;
    border-radius: 12px;
}

.feature-card h3 {
    color: #4f46e5;
}

.feature-card p {
    color: #64748b;
}

/* About section */
.about-section {
    max-width: 850px;
    margin: 0 auto;
    padding: 65px 24px;
    text-align: center;
}

.about-section p {
    color: #64748b;
}

/* Contact section */
.contact-section {
    padding: 65px 24px;
    background-color: #eef2ff;
    text-align: center;
}

.contact-section p {
    margin-bottom: 25px;
    color: #475569;
}

/* Footer */
.site-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 12px;
    padding: 22px 24px;
    color: white;
    background-color: #111827;
}

.site-footer p {
    margin: 0;
}

.site-footer a {
    color: #c7d2fe;
}

/* Responsive design */
@media (max-width: 760px) {
    .navbar {
        justify-content: center;
        flex-direction: column;
        gap: 16px;
        padding: 18px 14px;
    }

    .nav-links {
        justify-content: center;
        gap: 16px;
    }

    .hero {
        flex-direction: column;
        gap: 35px;
        min-height: auto;
        padding: 50px 20px;
    }

    .hero-content,
    .hero-image {
        width: 100%;
    }

    .hero-content {
        text-align: center;
    }

    .hero-content p {
        margin-right: auto;
        margin-left: auto;
    }

    .hero-actions {
        justify-content: center;
    }

    .hero-image img {
        height: 280px;
    }

    .site-footer {
        justify-content: center;
        flex-direction: column;
        text-align: center;
    }
}

@media (max-width: 420px) {
    .nav-links {
        gap: 12px;
    }

    .nav-links a {
        font-size: 14px;
    }

    .hero-content h1 {
        font-size: 32px;
    }

    .hero-content p {
        font-size: 15px;
    }

    .hero-image img {
        height: 220px;
    }
}

4. Explanation of Important CSS Properties

Property| Purpose
"display: flex"| Arranges the hero text and image side-by-side.
"justify-content: space-between"| Distributes space between the hero content and image.
"align-items: center"| Vertically aligns the hero text and image.
"flex-direction: column"| Stacks content vertically on smaller screens.
"flex-wrap: wrap"| Allows navigation links and buttons to wrap when needed.
"position: sticky"| Keeps the header at the top while scrolling.
"z-index: 1000"| Helps the sticky header appear above normal page content.
"object-fit: cover"| Fills the image area without distorting the image.
"@media"| Applies layout changes at smaller screen widths.

5. Result

The landing page was successfully created using HTML and CSS. It contains a logo, navigation links, a CTA button, a hero heading, descriptive text, an image, feature cards, a contact section, and a footer. Flexbox arranges the text and image side-by-side on wider screens and stacks them vertically on smaller screens.

6. Conclusion

In this assignment, I learned how to design a modern landing page header and hero section using CSS Flexbox. I practiced alignment, spacing, sticky positioning, image styling, CTA buttons, and responsive media queries to create a layout suitable for desktop and mobile devices.

7. Submission Checklist

- [ ] "Assignment-7.4.md"
- [ ] "index.html"
- [ ] "style.css"
- [ ] Screenshot of the landing page on desktop.
- [ ] Screenshot of the responsive layout on mobile.