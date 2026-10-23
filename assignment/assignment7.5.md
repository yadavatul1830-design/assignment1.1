Assignment 7.5 — Flexbox Mini-Project

1. Objective

The objective of this assignment is to build a complete, responsive landing page using HTML and CSS Flexbox. The landing page includes a navigation bar, hero section, three feature cards, a call-to-action section, and a footer. The design adapts to different screen sizes without content overflowing on smaller devices.

2. Questions and Answers

Q1. What is Flexbox?

Answer: Flexbox, or the Flexible Box Layout, is a CSS layout model used to arrange elements in rows or columns. It helps align, distribute, and space elements efficiently within a container.

Q2. What is the purpose of a navigation bar?

Answer: A navigation bar provides links to different sections of a website, such as Home, Features, About, and Contact.

Q3. What is a hero section?

Answer: A hero section is the main introductory section of a webpage. It usually contains a heading, description, call-to-action button, and an image or illustration.

Q4. What is the purpose of feature cards?

Answer: Feature cards present important information about a product, service, or website in separate, easy-to-read sections.

Q5. What is the use of the "gap" property in Flexbox?

Answer: The "gap" property creates consistent spacing between flex items without adding individual margins to each element.

Q6. What does "justify-content" do?

Answer: The "justify-content" property aligns and distributes flex items along the main axis of a flex container.

Q7. What does "align-items" do?

Answer: The "align-items" property aligns flex items along the cross axis of a flex container.

Q8. What is the purpose of "flex-wrap"?

Answer: The "flex-wrap" property allows flex items to move onto a new line when there is insufficient space in the container.

Q9. How can a webpage be made responsive?

Answer: A webpage can be made responsive using flexible layouts, Flexbox, relative units, suitable image sizing, and CSS media queries.

Q10. How do you prevent content overflow on small screens?

Answer: Content overflow can be prevented by using "max-width: 100%", "min-width: 0", flexible widths, "flex-wrap: wrap", and responsive media queries.

3. Project Structure

Create the following files in one folder:

Assignment-7.5/
├── index.html
└── style.css

4. HTML Code ("index.html")

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FlexStart - Build Your Future</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Navigation Bar -->
    <header class="navbar">
        <a href="#home" class="logo">FlexStart</a>

        <nav class="nav-links">
            <a href="#home">Home</a>
            <a href="#features">Features</a>
            <a href="#about">About</a>
            <a href="#contact">Contact</a>
        </nav>

        <a href="#contact" class="nav-button">Get Started</a>
    </header>

    <main>
        <!-- Hero Section -->
        <section class="hero" id="home">
            <div class="hero-content">
                <p class="eyebrow">WELCOME TO FLEXSTART</p>
                <h1>Build Something Amazing with Flexbox</h1>
                <p class="hero-description">
                    Create beautiful, flexible, and responsive web
                    experiences with a clean design and simple layout.
                </p>
                <div class="hero-buttons">
                    <a href="#features" class="button primary-button">
                        Explore Features
                    </a>
                    <a href="#about" class="button secondary-button">
                        Learn More
                    </a>
                </div>
            </div>

            <div class="hero-image">
                <img
                    src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=1000&q=80"
                    alt="Laptop displaying a web development workspace"
                >
            </div>
        </section>

        <!-- Features Section -->
        <section class="features section" id="features">
            <div class="section-heading">
                <p class="eyebrow">OUR FEATURES</p>
                <h2>Everything You Need to Get Started</h2>
                <p>
                    Discover the tools and ideas that make building
                    modern websites easier.
                </p>
            </div>

            <div class="feature-container">
                <article class="feature-card">
                    <div class="feature-icon">01</div>
                    <h3>Flexible Layout</h3>
                    <p>
                        Arrange content easily with Flexbox and create
                        layouts that adapt to available space.
                    </p>
                </article>

                <article class="feature-card">
                    <div class="feature-icon">02</div>
                    <h3>Responsive Design</h3>
                    <p>
                        Make your website look great on desktops,
                        tablets, and mobile devices.
                    </p>
                </article>

                <article class="feature-card">
                    <div class="feature-icon">03</div>
                    <h3>Clean Interface</h3>
                    <p>
                        Use consistent colors, typography, and spacing
                        to create a professional user experience.
                    </p>
                </article>
            </div>
        </section>

        <!-- About Section -->
        <section class="about section" id="about">
            <div>
                <p class="eyebrow">WHY FLEXSTART?</p>
                <h2>Designed for Simplicity and Growth</h2>
            </div>

            <p>
                FlexStart demonstrates how HTML and CSS can work
                together to create an attractive landing page.
                Flexbox helps organize content while responsive
                styling keeps the experience smooth on different
                screen sizes.
            </p>
        </section>

        <!-- Call-to-Action Section -->
        <section class="cta" id="contact">
            <div class="cta-content">
                <h2>Ready to Start Your Journey?</h2>
                <p>
                    Take the next step and turn your ideas into
                    something amazing.
                </p>
            </div>

            <a href="mailto:hello@example.com" class="button cta-button">
                Contact Us
            </a>
        </section>
    </main>

    <!-- Footer -->
    <footer class="footer">
        <a href="#home" class="footer-logo">FlexStart</a>
        <p>Learning today. Building tomorrow.</p>
        <p class="copyright">
            &copy; 2026 FlexStart. Created for a web development assignment.
        </p>
    </footer>

</body>
</html>

5. CSS Code ("style.css")

/* Global Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    scroll-padding-top: 90px;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background-color: #f8fafc;
    color: #172033;
    line-height: 1.6;
    overflow-wrap: break-word;
}

a {
    text-decoration: none;
}

img {
    display: block;
    max-width: 100%;
}

/* Navigation Bar */
.navbar {
    width: 100%;
    padding: 18px 7%;
    background-color: #ffffff;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 24px;
    flex-wrap: wrap;
    box-shadow: 0 2px 12px rgba(15, 23, 42, 0.06);
}

.logo,
.footer-logo {
    color: #4f46e5;
    font-size: 1.6rem;
    font-weight: 800;
    letter-spacing: -1px;
}

.nav-links {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 26px;
    flex-wrap: wrap;
}

.nav-links a {
    color: #475569;
    font-size: 0.95rem;
    font-weight: 600;
    transition: color 0.3s ease;
}

.nav-links a:hover {
    color: #4f46e5;
}

.nav-button {
    background-color: #4f46e5;
    color: #ffffff;
    padding: 10px 18px;
    border-radius: 8px;
    font-weight: 700;
    text-align: center;
}

.nav-button:hover,
.primary-button:hover {
    background-color: #3730a3;
}

/* Shared Button Styles */
.button {
    display: inline-block;
    padding: 13px 22px;
    border-radius: 8px;
    font-weight: 700;
    text-align: center;
    transition: background-color 0.3s ease;
}

.primary-button {
    background-color: #4f46e5;
    color: #ffffff;
}

.secondary-button {
    background-color: #e9eaff;
    color: #3730a3;
}

.secondary-button:hover {
    background-color: #dcdfff;
}

/* Hero Section */
.hero {
    padding: 80px 7%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 48px;
    flex-wrap: wrap;
}

.hero-content {
    flex: 1 1 320px;
    min-width: 0;
}

.eyebrow {
    color: #4f46e5;
    font-size: 0.82rem;
    font-weight: 800;
    letter-spacing: 2px;
    margin-bottom: 14px;
}

.hero h1 {
    max-width: 600px;
    font-size: clamp(2.2rem, 5vw, 3.8rem);
    line-height: 1.15;
    letter-spacing: -1.5px;
    margin-bottom: 20px;
}

.hero-description {
    max-width: 520px;
    color: #64748b;
    font-size: 1.08rem;
    margin-bottom: 28px;
}

.hero-buttons {
    display: flex;
    align-items: center;
    gap: 14px;
    flex-wrap: wrap;
}

.hero-image {
    flex: 1 1 320px;
    min-width: 0;
}

.hero-image img {
    width: 100%;
    min-height: 280px;
    max-height: 420px;
    object-fit: cover;
    border-radius: 20px;
    box-shadow: 0 20px 45px rgba(15, 23, 42, 0.12);
}

/* Shared Section Styles */
.section {
    padding: 75px 7%;
}

.section-heading {
    max-width: 680px;
    margin: 0 auto 42px;
    text-align: center;
}

.section-heading h2,
.about h2 {
    font-size: clamp(1.8rem, 4vw, 2.5rem);
    line-height: 1.25;
    margin-bottom: 16px;
}

.section-heading > p:last-child {
    color: #64748b;
}

/* Feature Cards */
.features {
    background-color: #ffffff;
}

.feature-container {
    display: flex;
    justify-content: center;
    align-items: stretch;
    gap: 24px;
    flex-wrap: wrap;
}

.feature-card {
    flex: 1 1 250px;
    min-width: 0;
    padding: 30px;
    background-color: #f8fafc;
    border: 1px solid #e2e8f0;
    border-radius: 16px;
    transition: transform 0.3s ease,
                box-shadow 0.3s ease;
}

.feature-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 12px 28px rgba(15, 23, 42, 0.08);
}

.feature-icon {
    width: 52px;
    height: 52px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #e9eaff;
    color: #4f46e5;
    border-radius: 12px;
    font-weight: 800;
    margin-bottom: 20px;
}

.feature-card h3 {
    font-size: 1.25rem;
    margin-bottom: 12px;
}

.feature-card p {
    color: #64748b;
}

/* About Section */
.about {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 40px;
    flex-wrap: wrap;
}

.about > div,
.about > p {
    flex: 1 1 280px;
    min-width: 0;
}

.about > p {
    color: #64748b;
    font-size: 1.05rem;
}

/* Call-to-Action Section */
.cta {
    margin: 20px 7% 75px;
    padding: 48px;
    background-color: #4f46e5;
    color: #ffffff;
    border-radius: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 28px;
    flex-wrap: wrap;
}

.cta-content {
    flex: 1 1 280px;
    min-width: 0;
}

.cta h2 {
    font-size: clamp(1.6rem, 3vw, 2.2rem);
    line-height: 1.25;
    margin-bottom: 12px;
}

.cta p {
    color: #e0e7ff;
}

.cta-button {
    background-color: #ffffff;
    color: #3730a3;
    flex-shrink: 0;
}

.cta-button:hover {
    background-color: #e9eaff;
}

/* Footer */
.footer {
    padding: 35px 7%;
    background-color: #111827;
    color: #cbd5e1;
    text-align: center;
}

.footer-logo {
    display: inline-block;
    margin-bottom: 8px;
}

.copyright {
    margin-top: 12px;
    font-size: 0.85rem;
    color: #94a3b8;
}

/* Responsive Design */
@media (max-width: 768px) {
    .navbar {
        justify-content: center;
        text-align: center;
    }

    .nav-links {
        order: 3;
        width: 100%;
        gap: 16px;
    }

    .hero {
        padding-top: 55px;
        padding-bottom: 55px;
        gap: 32px;
    }

    .hero-content,
    .hero-image {
        flex-basis: 100%;
    }

    .hero-image img {
        min-height: 220px;
    }

    .section {
        padding-top: 55px;
        padding-bottom: 55px;
    }

    .cta {
        padding: 32px;
        margin-bottom: 55px;
    }
}

@media (max-width: 480px) {
    .navbar {
        padding: 18px 5%;
        gap: 14px;
    }

    .nav-links {
        gap: 12px;
    }

    .nav-links a {
        font-size: 0.88rem;
    }

    .hero,
    .section {
        padding-left: 5%;
        padding-right: 5%;
    }

    .hero-buttons {
        align-items: stretch;
    }

    .hero-buttons .button {
        flex: 1 1 100%;
    }

    .feature-card {
        flex-basis: 100%;
        padding: 24px;
    }

    .cta {
        margin-left: 5%;
        margin-right: 5%;
        padding: 26px 22px;
    }

    .cta-button {
        width: 100%;
    }

    .footer {
        padding: 30px 5%;
    }
}

6. Explanation of Important CSS Properties

Property| Purpose
"display: flex"| Creates a Flexbox layout.
"justify-content"| Controls the distribution of items along the main axis.
"align-items"| Aligns items along the cross axis.
"gap"| Adds consistent spacing between items.
"flex-wrap: wrap"| Allows items to move to the next line when necessary.
"flex: 1 1 320px"| Allows an item to grow and shrink, with a preferred base size of 320px.
"min-width: 0"| Allows flex children to shrink below their automatic minimum width.
"max-width: 100%"| Prevents images from exceeding their container's width.
"@media"| Applies CSS rules at specific screen widths.
"box-sizing: border-box"| Includes padding and borders in an element's declared dimensions.

7. Result

The completed landing page contains:

1. A responsive navigation bar with working section links.
2. A hero section with a heading, description, buttons, and image.
3. Three feature cards arranged in a responsive row.
4. An about section describing the project.
5. A call-to-action section with a contact button.
6. A footer with the project name and copyright text.

Flexbox is used to align the navigation items, arrange the hero content, display feature cards, and organize the call-to-action section. Media queries adjust the layout for smaller screens.

8. Conclusion

This assignment demonstrates how Flexbox can be used to build a complete, responsive landing page using HTML and CSS. The project uses "gap", "justify-content", "align-items", and "flex-wrap" to create flexible layouts. Consistent colors, typography, and spacing improve the design, while responsive rules help prevent content overflow on smaller screens.

9. Submission Checklist

- [ ] Save the HTML file as "index.html".
- [ ] Save the CSS file as "style.css".
- [ ] Keep both files in the same folder.
- [ ] Open the webpage in a browser and check all sections.
- [ ] Test the layout at desktop and mobile screen sizes.
- [ ] Take actual screenshots of the completed webpage.
- [ ] Upload both files to a GitHub repository.
- [ ] Submit the repository link along with the assignment.