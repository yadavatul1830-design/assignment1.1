Assignment 9.2 — Responsive Typography & Images

Q1. How do you create an article or portfolio webpage?

Answer: An article or portfolio webpage presents information using headings, paragraphs, and images. It should be easy to read on mobile phones, tablets, and desktops.

Q2. How do you add headings, paragraphs, and images in HTML?

Answer: We use heading tags, paragraph tags, and the image tag to display text and pictures.

<h1>My Portfolio</h1>
<h2>About Me</h2>
<p>I am a student interested in web development.</p>
<img src="images/profile.jpg" alt="Profile photograph">

Q3. How do you use "rem", "em", or "clamp()" for responsive font sizes?

Answer: These units help adjust text sizes.

- "rem" sets a size relative to the root font size.
- "em" sets a size relative to the parent element's font size.
- "clamp()" sets a minimum, preferred, and maximum size.

Example:

h1 {
    font-size: clamp(2rem, 5vw, 3rem);
}

p {
    font-size: 1rem;
    line-height: 1.7;
}

Q4. How do you make images responsive?

Answer: Use "max-width: 100%" and "height: auto" so images fit their containers without stretching.

img {
    max-width: 100%;
    height: auto;
    display: block;
}

Q5. Why should a content container have a suitable "max-width"?

Answer: A maximum width prevents text from spreading across the entire screen on large displays. It keeps the content readable.

.container {
    width: 100%;
    max-width: 900px;
    margin: 0 auto;
    padding: 20px;
}

Q6. How do you improve text length and spacing on mobile and desktop?

Answer: Use suitable line spacing, margins, padding, and responsive font sizes. Keep paragraphs short enough to read comfortably and leave enough space between sections.

p {
    line-height: 1.7;
    margin-bottom: 1rem;
}

@media (min-width: 768px) {
    .container {
        padding: 32px;
    }
}

Q7. How do you check that images do not stretch and text does not overflow?

Answer: Open the webpage in Chrome and use Developer Tools' Device Mode to test mobile and desktop widths. Check that images keep their proportions and text remains inside the screen. Fix any overflow using flexible widths and responsive CSS.

---

Practical Implementation

Create two files: "index.html" and "style.css".

File 1: "index.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Portfolio</title>
    <meta name="description" content="A responsive student portfolio with readable typography and images.">
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="header">
        <h1>My Portfolio</h1>
        <p>Learning, Creating, and Growing</p>
    </header>

    <main class="container">
        <section class="intro">
            <h2>About Me</h2>
            <p>
                Hello! I am a student who enjoys learning new skills,
                exploring technology, and creating useful projects.
                This portfolio shares my interests and work.
            </p>

            <img
                src="https://placehold.co/900x400?text=My+Portfolio"
                alt="Portfolio banner showing a creative workspace">
        </section>

        <section>
            <h2>My Interests</h2>
            <p>
                I am interested in web design, programming, teamwork,
                and solving problems. I enjoy learning through practical
                activities and improving my skills step by step.
            </p>
        </section>

        <section class="project">
            <h2>My Project</h2>
            <img
                src="https://placehold.co/800x450?text=Web+Design+Project"
                alt="Preview of a web design project">

            <h3>Responsive Website</h3>
            <p>
                This project demonstrates how text, images, and content
                adjust to different screen sizes using HTML and CSS.
            </p>
        </section>
    </main>

    <footer class="footer">
        <p>&copy; 2026 My Portfolio</p>
    </footer>

</body>
</html>

File 2: "style.css"

/* General settings */
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    font-size: 1rem;
    line-height: 1.7;
    color: #222;
    background-color: #f4f7fb;
    overflow-wrap: anywhere;
}

/* Responsive header */
.header {
    text-align: center;
    padding: 24px 16px;
    background-color: #24476b;
    color: white;
}

h1 {
    font-size: clamp(2rem, 5vw, 3rem);
    line-height: 1.2;
}

h2 {
    font-size: clamp(1.4rem, 3vw, 2rem);
}

h3 {
    font-size: 1.25rem;
}

/* Content container */
.container {
    width: 100%;
    max-width: 900px;
    margin: 0 auto;
    padding: 16px;
}

section {
    margin-bottom: 28px;
}

p {
    font-size: 1rem;
    line-height: 1.7;
    margin-bottom: 16px;
}

/* Responsive images */
img {
    display: block;
    max-width: 100%;
    height: auto;
    border-radius: 8px;
}

/* Footer */
.footer {
    text-align: center;
    padding: 12px;
    background-color: #24476b;
    color: white;
}

/* Tablet and desktop adjustments */
@media (min-width: 768px) {
    .container {
        padding: 28px;
    }

    section {
        margin-bottom: 36px;
    }

    p {
        font-size: 1.05rem;
    }
}

@media (min-width: 1024px) {
    .container {
        max-width: 900px;
    }
}

Submission Checklist

1. Save the assignment as "Assignment-9.2.md".
2. Save the HTML code as "index.html".
3. Save the CSS code as "style.css" in the same folder.
4. Open "index.html" in a browser and verify that the images load.
5. Use Chrome DevTools Device Mode to check the mobile and desktop layouts.
6. Take one mobile screenshot and one desktop screenshot.
7. Submit both files and the screenshots.

Expected result: Text adjusts to screen size, images fit their containers without stretching, and the content remains readable on mobile and desktop.