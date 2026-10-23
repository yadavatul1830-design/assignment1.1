Assignment 8.5 — CSS Grid Mini-Project

1. Objective

The objective of this assignment is to create a complete responsive photo-gallery website using HTML and CSS Grid. The project demonstrates the use of "repeat()", "minmax()", fractional ("fr") units, named grid areas, consistent gaps, and responsive columns. It also ensures that images and text remain within their containers on different screen sizes.

2. Questions and Answers

Q1. What is CSS Grid?

Answer: CSS Grid is a two-dimensional CSS layout system that arranges elements into rows and columns. It is useful for creating structured and responsive webpage layouts.

Q2. What is the purpose of a photo gallery website?

Answer: A photo gallery website displays images in an organized layout, allowing users to view photographs in a visually appealing manner.

Q3. What is the "grid-template-columns" property?

Answer: The "grid-template-columns" property defines the number, size, and arrangement of columns in a CSS Grid container.

Q4. What is the purpose of the "repeat()" function?

Answer: The "repeat()" function simplifies Grid definitions by repeating a column or row pattern multiple times.

Example:

grid-template-columns: repeat(3, 1fr);

This creates three equal-width columns.

Q5. What does "minmax()" do in CSS Grid?

Answer: The "minmax()" function defines a minimum and maximum size for a Grid track. It helps create flexible layouts that adapt to available space.

Example:

grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));

Q6. What is the "fr" unit?

Answer: The "fr" unit represents a fraction of the available space in a Grid container. It allows columns and rows to share available space proportionally.

Q7. What are named grid areas?

Answer: Named grid areas allow developers to assign names to specific sections of a Grid layout using "grid-template-areas". This makes the layout easier to understand and manage.

Q8. What is the purpose of the "gap" property?

Answer: The "gap" property creates consistent spacing between Grid rows and columns without requiring individual margins on each card.

Q9. How can image overflow be prevented?

Answer: Image overflow can be prevented by setting "max-width: 100%", using "width: 100%", and applying "object-fit: cover" when an image needs to fill a fixed-size container.

Q10. How can a CSS Grid layout be made responsive?

Answer: A Grid layout can be made responsive by using "repeat()", "minmax()", "auto-fit", fractional units, and media queries to adjust the number of columns according to screen width.

3. Project Structure

Create the following files in the same folder:

Assignment-8.5/
├── index.html
└── style.css

4. HTML Code ("index.html")

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FrameSpace - Photo Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Main Grid Layout -->
    <div class="page-layout">

        <!-- Header -->
        <header class="header">
            <a href="#home" class="logo">FrameSpace<span>.</span></a>

            <nav class="navigation">
                <a href="#home">Home</a>
                <a href="#gallery">Gallery</a>
                <a href="#about">About</a>
            </nav>

            <a href="#gallery" class="header-button">Explore Photos</a>
        </header>

        <!-- Main Content -->
        <main class="main-content" id="home">

            <!-- Hero Section -->
            <section class="hero">
                <p class="eyebrow">A COLLECTION OF MOMENTS</p>
                <h1>Discover Beauty in Every Frame.</h1>
                <p>
                    Explore a curated collection of nature, architecture,
                    travel, and everyday moments captured through photography.
                </p>
                <a href="#gallery" class="hero-button">View Gallery &rarr;</a>
            </section>

            <!-- Gallery Section -->
            <section class="gallery-section" id="gallery">

                <div class="section-heading">
                    <div>
                        <p class="eyebrow">OUR COLLECTION</p>
                        <h2>Photo Gallery</h2>
                    </div>
                    <p class="gallery-count">09 Photographs</p>
                </div>

                <div class="gallery-grid">

                    <article class="photo-card featured">
                        <img
                            src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?auto=format&fit=crop&w=1200&q=80"
                            alt="Mountain landscape beside a peaceful lake"
                            loading="lazy"
                        >
                        <div class="photo-info">
                            <span>01 / NATURE</span>
                            <h3>Peaceful Mountains</h3>
                        </div>
                    </article>

                    <article class="photo-card">
                        <img
                            src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=900&q=80"
                            alt="Beautiful outdoor landscape"
                            loading="lazy"
                        >
                        <div class="photo-info">
                            <span>02 / TRAVEL</span>
                            <h3>Open Horizons</h3>
                        </div>
                    </article>

                    <article class="photo-card">
                        <img
                            src="https://images.unsplash.com/photo-1518837695005-2083093ee35b?auto=format&fit=crop&w=900&q=80"
                            alt="Ocean waves moving toward the shore"
                            loading="lazy"
                        >
                        <div class="photo-info">
                            <span>03 / OCEAN</span>
                            <h3>Ocean Waves</h3>
                        </div>
                    </article>

                    <article class="photo-card">
                        <img
                            src="https://images.unsplash.com/photo-1519608487953-e999c86e7455?auto=format&fit=crop&w=900&q=80"
                            alt="Night sky filled with stars"
                            loading="lazy"
                        >
                        <div class="photo-info">
                            <span>04 / NIGHT</span>
                            <h3>Under the Stars</h3>
                        </div>
                    </article>

                    <article class="photo-card">
                        <img
                            src="https://images.unsplash.com/photo-1511818966892-d7d671e672a2?auto=format&fit=crop&w=900&q=80"
                            alt="Modern architectural building"
                            loading="lazy"
                        >
                        <div class="photo-info">
                            <span>05 / DESIGN</span>
                            <h3>Modern Architecture</h3>
                        </div>
                    </article>

                    <article class="photo-card">
                        <img
                            src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?auto=format&fit=crop&w=900&q=80"
                            alt="Sunlight passing through a green forest"
                            loading="lazy"
                        >
                        <div class="photo-info">
                            <span>06 / FOREST</span>
                            <h3>Into the Forest</h3>
                        </div>
                    </article>

                    <article class="photo-card">
                        <img
                            src="https://images.unsplash.com/photo-1470252649378-9c29740c9fa8?auto=format&fit=crop&w=900&q=80"
                            alt="Warm sunlight across a natural landscape"
                            loading="lazy"
                        >
                        <div class="photo-info">
                            <span>07 / SUNRISE</span>
                            <h3>Golden Morning</h3>
                        </div>
                    </article>

                    <article class="photo-card">
                        <img
                            src="https://images.unsplash.com/photo-1472214103451-9374bd1c798e?auto=format&fit=crop&w=900&q=80"
                            alt="Green hills under a wide open sky"
                            loading="lazy"
                        >
                        <div class="photo-info">
                            <span>08 / LANDSCAPE</span>
                            <h3>Green Valley</h3>
                        </div>
                    </article>

                    <article class="photo-card">
                        <img
                            src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?auto=format&fit=crop&w=900&q=80"
                            alt="Scenic mountain lake and surrounding landscape"
                            loading="lazy"
                        >
                        <div class="photo-info">
                            <span>09 / ADVENTURE</span>
                            <h3>Into the Wild</h3>
                        </div>
                    </article>

                </div>
            </section>

            <!-- About Section -->
            <section class="about-section" id="about">
                <div>
                    <p class="eyebrow">ABOUT FRAMESPACE</p>
                    <h2>Every picture tells a story.</h2>
                </div>
                <p>
                    FrameSpace is a sample photography gallery created
                    to demonstrate CSS Grid, responsive image cards,
                    and a consistent visual design using HTML and CSS.
                </p>
            </section>

        </main>

        <!-- Footer -->
        <footer class="footer">
            <a href="#home" class="logo">FrameSpace<span>.</span></a>
            <p>Collect moments. Create memories.</p>
            <p class="copyright">
                &copy; 2026 FrameSpace. Created for a CSS Grid assignment.
            </p>
        </footer>

    </div>

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
    scroll-padding-top: 25px;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    color: #1e293b;
    background: #f8fafc;
    line-height: 1.6;
    overflow-wrap: break-word;
}

a {
    color: inherit;
    text-decoration: none;
}

img {
    display: block;
    max-width: 100%;
}

/* Primary Grid Layout with Named Areas */
.page-layout {
    min-height: 100vh;
    display: grid;

    grid-template-columns: minmax(0, 1fr);
    grid-template-rows: auto 1fr auto;

    grid-template-areas:
        "header"
        "main"
        "footer";
}

/* Header */
.header {
    grid-area: header;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 24px;
    flex-wrap: wrap;

    padding: 22px 7%;
    background: #ffffff;
    border-bottom: 1px solid #e2e8f0;
}

.logo {
    font-size: 1.65rem;
    font-weight: 800;
    letter-spacing: -1px;
    color: #172033;
}

.logo span {
    color: #e87952;
}

.navigation {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 28px;
    flex-wrap: wrap;
}

.navigation a {
    color: #64748b;
    font-size: 0.93rem;
    font-weight: 600;
}

.navigation a:hover {
    color: #e87952;
}

.header-button {
    padding: 10px 16px;
    background: #172033;
    color: #ffffff;
    border-radius: 7px;
    font-size: 0.88rem;
    font-weight: 700;
}

/* Main Content */
.main-content {
    grid-area: main;
    min-width: 0;
}

/* Hero Section */
.hero {
    padding: 75px 7% 65px;
    text-align: center;
    background: #f1f5f9;
}

.eyebrow {
    color: #d65d38;
    font-size: 0.75rem;
    font-weight: 800;
    letter-spacing: 2px;
    margin-bottom: 12px;
}

.hero h1 {
    max-width: 800px;
    margin: 0 auto 18px;
    font-size: clamp(2.2rem, 5vw, 4rem);
    line-height: 1.12;
    letter-spacing: -1.8px;
}

.hero > p:not(.eyebrow) {
    max-width: 620px;
    margin: 0 auto 25px;
    color: #64748b;
    font-size: 1.03rem;
}

.hero-button {
    display: inline-block;
    padding: 12px 22px;
    background: #e87952;
    color: #ffffff;
    border-radius: 7px;
    font-weight: 700;
}

.hero-button:hover {
    background: #c85f3a;
}

/* Gallery Section */
.gallery-section {
    padding: 65px 7%;
}

.section-heading {
    display: flex;
    justify-content: space-between;
    align-items: end;
    gap: 20px;
    flex-wrap: wrap;
    margin-bottom: 28px;
}

.section-heading h2,
.about-section h2 {
    font-size: clamp(1.8rem, 4vw, 2.5rem);
    line-height: 1.2;
}

.gallery-count {
    color: #64748b;
    font-size: 0.88rem;
}

/* Responsive Grid with repeat(), minmax(), and fr */
.gallery-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 24px;
    align-items: stretch;
}

/* Explicit Grid Placement */
.photo-card.featured {
    grid-column: span 2;
}

.photo-card {
    min-width: 0;
    overflow: hidden;
    background: #ffffff;
    border: 1px solid #e2e8f0;
    border-radius: 13px;
    box-shadow: 0 5px 18px rgba(15, 23, 42, 0.04);
    transition: transform 0.25s ease,
                box-shadow 0.25s ease;
}

.photo-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 12px 25px rgba(15, 23, 42, 0.1);
}

.photo-card img {
    width: 100%;
    height: 220px;
    object-fit: cover;
    background: #e2e8f0;
}

.photo-card.featured img {
    height: 280px;
}

.photo-info {
    padding: 17px 18px 20px;
    min-width: 0;
}

.photo-info span {
    display: block;
    margin-bottom: 7px;
    color: #d65d38;
    font-size: 0.68rem;
    font-weight: 800;
    letter-spacing: 1.2px;
}

.photo-info h3 {
    font-size: 1.05rem;
    overflow-wrap: anywhere;
}

/* About Section */
.about-section {
    padding: 45px 7% 65px;
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 40px;
    align-items: center;
    background: #ffffff;
}

.about-section > p {
    color: #64748b;
    font-size: 1rem;
    min-width: 0;
}

/* Footer */
.footer {
    grid-area: footer;
    padding: 35px 7%;
    text-align: center;
    background: #172033;
    color: #cbd5e1;
}

.footer .logo {
    display: inline-block;
    color: #ffffff;
    margin-bottom: 8px;
}

.footer > p {
    font-size: 0.9rem;
}

.footer .copyright {
    margin-top: 12px;
    color: #94a3b8;
    font-size: 0.8rem;
}

/* Tablet: Two Columns */
@media (max-width: 900px) {
    .header {
        padding-left: 5%;
        padding-right: 5%;
    }

    .gallery-section {
        padding-left: 5%;
        padding-right: 5%;
    }

    .gallery-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 18px;
    }

    .photo-card.featured {
        grid-column: span 2;
    }

    .about-section {
        padding-left: 5%;
        padding-right: 5%;
        gap: 25px;
    }
}

/* Mobile: Single Column */
@media (max-width: 560px) {
    .header {
        justify-content: center;
        text-align: center;
        gap: 16px;
    }

    .navigation {
        order: 3;
        width: 100%;
        gap: 18px;
    }

    .hero {
        padding: 55px 6%;
    }

    .hero h1 {
        letter-spacing: -1px;
    }

    .gallery-section {
        padding: 45px 5%;
    }

    .gallery-grid {
        grid-template-columns: minmax(0, 1fr);
        gap: 18px;
    }

    .photo-card.featured {
        grid-column: auto;
    }

    .photo-card img,
    .photo-card.featured img {
        height: 230px;
    }

    .about-section {
        grid-template-columns: minmax(0, 1fr);
        gap: 18px;
        padding: 40px 6%;
    }

    .footer {
        padding: 30px 5%;
    }
}

6. Explanation of Important CSS Properties

Property| Purpose
"display: grid"| Creates a CSS Grid container.
"grid-template-areas"| Defines named areas for the header, main content, and footer.
"grid-column: span 2"| Makes the featured photo card span two columns.
"repeat()"| Repeats a column pattern without writing it multiple times.
"minmax(0, 1fr)"| Allows columns to share available space while having a zero minimum track size.
"fr"| Distributes available space proportionally between Grid tracks.
"gap"| Creates consistent spacing between cards and sections.
"object-fit: cover"| Fills an image container while preserving the image's aspect ratio.
"max-width: 100%"| Prevents images from exceeding their container width.
"overflow-wrap: anywhere"| Allows long text to wrap rather than expanding the layout.
"@media"| Adjusts the layout for tablet and mobile screen widths.

7. Responsive Design

The project uses three layout stages:

- Desktop: Three columns in the photo gallery.
- Tablet: Two columns.
- Mobile: One column.

The featured photo spans two columns on desktop and tablet. On mobile, it returns to a single column so that the gallery fits smaller screens.

8. Result

The completed project displays a photo gallery website with a header, navigation links, introductory hero section, multiple photo cards, an about section, and a footer.

CSS Grid is used as the primary layout system. The project demonstrates named grid areas, explicit grid placement, "repeat()", "minmax()", "fr" units, and consistent gaps. Responsive media queries adjust the number of columns to improve usability on smaller screens.

9. Conclusion

This assignment demonstrates how CSS Grid can be used to build a complete and responsive photo-gallery website. Flexible Grid tracks, named areas, explicit placement, and responsive breakpoints create an organized layout. Image sizing and text wrapping help prevent overflow, while consistent spacing and typography improve the overall design.

10. Submission Checklist

- [ ] Save the HTML file as "index.html".
- [ ] Save the CSS file as "style.css".
- [ ] Keep both files in the same folder.
- [ ] Open the webpage in a browser.
- [ ] Check that all images load correctly.
- [ ] Test the layout at desktop, tablet, and mobile widths.
- [ ] Upload both files to a GitHub repository.
- [ ] Copy the actual GitHub repository URL for submission.