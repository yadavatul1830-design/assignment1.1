Assignment 3.1 — Two-Page Website with Working Links

Q1. Create "index.html" and "about.html" files.

Answer: I created two HTML files named "index.html" and "about.html" to build a simple two-page website.

Q2. Create the website name, introduction, and a navigation bar on the home page.

Answer: I added the website name, a short introduction, and a navigation bar to the home page using HTML headings, paragraphs, and links.

Q3. Add Home and About links in the navigation.

Answer: I added Home and About links in the navigation bar so users can move between the two pages.

Q4. Connect both pages using "<a href="">".

Answer: I used the anchor tag "<a>" with the "href" attribute to connect "index.html" and "about.html".

Q5. Add a link to an external website.

Answer: I added a link to an external website, such as Google, using the anchor tag.

Q6. Use "target="_blank"" and "rel="noopener noreferrer"" for the external link.

Answer: I used "target="_blank"" to open the external website in a new tab and "rel="noopener noreferrer"" to improve security.

HTML Code

1. "index.html" — Home Page

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Personal Website - Home</title>
</head>
<body>

    <header>
        <h1>My Personal Website</h1>
        <p>Welcome to my website!</p>
    </header>

    <nav>
        <a href="index.html">Home</a> |
        <a href="about.html">About</a>
    </nav>

    <hr>

    <main>
        <h2>Introduction</h2>
        <p>Hello! My name is Radhika Singh. I am learning HTML
        and web development. This is my first two-page website.</p>

        <p>
            Visit
            <a href="https://www.google.com/"
               target="_blank"
               rel="noopener noreferrer">Google</a>
            to explore the internet.
        </p>
    </main>

    <footer>
        <p>Thank you for visiting my website!</p>
    </footer>

</body>
</html>

2. "about.html" — About Page

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Personal Website - About</title>
</head>
<body>

    <header>
        <h1>About Me</h1>
    </header>

    <nav>
        <a href="index.html">Home</a> |
        <a href="about.html">About</a>
    </nav>

    <hr>

    <main>
        <h2>Who Am I?</h2>
        <p>My name is Radhika Singh, and I am a BBA student
        at Invertis University.</p>

        <p>I enjoy learning new skills, reading books, and
        exploring technology.</p>
    </main>

    <footer>
        <p>Thank you for visiting the About page!</p>
    </footer>

</body>
</html>

Submission

1. "index.html" — Home page.
2. "about.html" — About page.
3. Screenshot showing the website and working navigation links.

How to test: Save both files in the same folder. Open "index.html" in a browser, click About, and then click Home to check that both links work. Click Google to confirm that the external link opens in a new tab.