Assignment 5.3 — Typography Showcase Page

Objective

To create a typography showcase webpage using Google Fonts and different CSS typography properties.

Question 1: Select two complementary font families from Google Fonts.

Answer:

I selected Poppins for headings and Roboto for body text. Poppins gives headings a modern appearance, while Roboto makes paragraphs clear and readable.

The fonts are imported from Google Fonts using the following code:

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Roboto:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">

Question 2: Set different fonts for heading and body text.

Answer:

The "font-family" property is used to set different fonts for headings and body text.

h1, h2, h3 {
    font-family: 'Poppins', sans-serif;
}

body {
    font-family: 'Roboto', sans-serif;
}

Question 3: Use different font sizes and weights.

Answer:

The "font-size" property controls the size of text, while the "font-weight" property controls its thickness.

h1 {
    font-size: 42px;
    font-weight: 700;
}

h2 {
    font-size: 28px;
    font-weight: 600;
}

p {
    font-size: 16px;
    font-weight: 400;
}

Question 4: Apply "text-align", "text-decoration", and "font-style".

Answer:

These properties control text alignment, decoration, and style.

h1 {
    text-align: center;
}

a {
    text-decoration: none;
}

.emphasis {
    font-style: italic;
}

Question 5: Adjust "letter-spacing" and "line-height".

Answer:

The "letter-spacing" property controls the space between letters, and "line-height" controls the spacing between lines of text.

h1 {
    letter-spacing: 2px;
}

p {
    line-height: 1.8;
}

Question 6: Create three sections: Heading Styles, Paragraph Styles, and Text Emphasis.

Answer:

The following HTML and CSS create a typography showcase webpage with all three required sections.

HTML File ("index.html")

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Typography Showcase</title>

    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Roboto:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">

    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>Typography Showcase</h1>
        <p class="subtitle">Exploring the beauty of fonts and text styles</p>
    </header>

    <main>
        <section class="showcase">
            <h2>1. Heading Styles</h2>
            <h1 class="sample-heading">Main Heading</h1>
            <h2 class="sample-subheading">Subheading Example</h2>
            <h3 class="small-heading">Small Heading</h3>
        </section>

        <section class="showcase">
            <h2>2. Paragraph Styles</h2>
            <p class="normal-text">
                Typography is an important part of web design.
                It helps make content clear, readable, and attractive.
            </p>

            <p class="large-text">
                Good typography improves the user experience
                and makes information easier to understand.
            </p>
        </section>

        <section class="showcase">
            <h2>3. Text Emphasis</h2>
            <p>This is a <strong>bold text</strong> example.</p>
            <p class="italic-text">This is an italic text example.</p>
            <p class="underline-text">This is an underlined text example.</p>
            <p class="spaced-text">TEXT WITH LETTER SPACING</p>
            <a href="#top">This is a sample link</a>
        </section>
    </main>

    <footer>
        <p>Created for Assignment 5.3 — Typography Showcase Page</p>
    </footer>

</body>
</html>

CSS File ("style.css")

/* General Styling */
* {
    box-sizing: border-box;
}

body {
    font-family: 'Roboto', sans-serif;
    background-color: #f4f6f9;
    color: #333333;
    margin: 0;
    padding: 20px;
    line-height: 1.8;
}

/* Header Styling */
header {
    text-align: center;
    background-color: #1e3a5f;
    color: white;
    padding: 30px 15px;
    border-radius: 10px;
}

header h1 {
    font-family: 'Poppins', sans-serif;
    font-size: 42px;
    font-weight: 700;
    letter-spacing: 2px;
    margin-bottom: 5px;
}

.subtitle {
    font-size: 18px;
    font-style: italic;
}

/* Section Styling */
.showcase {
    background-color: white;
    padding: 25px;
    margin: 25px 0;
    border-radius: 10px;
    box-shadow: 0 2px 8px #dddddd;
}

.showcase h2 {
    font-family: 'Poppins', sans-serif;
    color: #1e3a5f;
    font-size: 28px;
    font-weight: 600;
    border-bottom: 2px solid #1e3a5f;
    padding-bottom: 8px;
}

/* Heading Styles */
.sample-heading {
    font-family: 'Poppins', sans-serif;
    font-size: 36px;
    font-weight: 700;
    text-align: left;
}

.sample-subheading {
    font-family: 'Poppins', sans-serif;
    font-size: 28px;
    font-weight: 600;
}

.small-heading {
    font-family: 'Poppins', sans-serif;
    font-size: 22px;
    font-weight: 500;
}

/* Paragraph Styles */
.normal-text {
    font-size: 16px;
    font-weight: 400;
    line-height: 1.8;
}

.large-text {
    font-size: 20px;
    font-weight: 400;
    line-height: 2;
}

/* Text Emphasis */
.italic-text {
    font-style: italic;
}

.underline-text {
    text-decoration: underline;
}

.spaced-text {
    letter-spacing: 3px;
    font-weight: 700;
}

strong {
    font-weight: 700;
}

a {
    color: #0066cc;
    text-decoration: none;
    font-weight: 700;
}

a:hover {
    text-decoration: underline;
}

/* Footer Styling */
footer {
    text-align: center;
    font-size: 14px;
    color: #666666;
    padding: 15px;
}

Result

The typography showcase webpage was created successfully using two Google Fonts, Poppins and Roboto. Different font sizes, font weights, text alignments, text decorations, font styles, letter spacing, and line heights were applied. The webpage contains the three required sections: Heading Styles, Paragraph Styles, and Text Emphasis.

Conclusion

This assignment helped me understand how typography improves the readability and appearance of a webpage. I learned how to use Google Fonts and apply different CSS typography properties to create a clean and attractive design.

Submission

1. "index.html" — Contains the typography showcase webpage.
2. "style.css" — Contains all CSS typography and layout styling.
3. "Assignment-5.3.md" — Contains the questions, answers, result, and conclusion.