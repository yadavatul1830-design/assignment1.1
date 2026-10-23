Assignment 5.1 — Convert an HTML Page into a Styled Page

Objective

To add CSS styling to the HTML website created in Week 4 using an external CSS stylesheet.

1. Create a "style.css" File

Create a new file named "style.css" in the same folder as the "index.html" file. This file will contain all the CSS styling rules for the webpage.

2. Link the External Stylesheet in HTML

Add the following line inside the "<head>" section of "index.html":

<link rel="stylesheet" href="style.css">

This connects the external CSS file to the HTML webpage.

3. Set the Body Background, Text Color, and Font

The following CSS sets the background color, text color, and font of the webpage:

body {
    background-color: #f4f7fa;
    color: #333333;
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
}

4. Style Headings, Paragraphs, and Links

Use CSS to make headings, paragraphs, and links more attractive and readable.

h1 {
    color: #1a5276;
    text-align: center;
    font-size: 32px;
}

h2 {
    color: #2874a6;
    font-size: 24px;
}

p {
    font-size: 16px;
    line-height: 1.6;
}

a {
    color: #0077cc;
    text-decoration: none;
}

a:hover {
    color: #e67e22;
    text-decoration: underline;
}

5. Make Navigation Links Readable and Attractive

The following CSS styles the navigation bar and its links:

nav {
    background-color: #1a5276;
    padding: 15px;
    text-align: center;
}

nav a {
    color: white;
    text-decoration: none;
    margin: 0 15px;
    font-weight: bold;
}

nav a:hover {
    color: #f1c40f;
}

6. Inspect Styles Using Chrome DevTools

The webpage can be inspected using Chrome Developer Tools.

Steps:

1. Open "index.html" in Google Chrome.
2. Right-click anywhere on the webpage and select Inspect.
3. Open the Elements tab to view the HTML elements.
4. Select an element and check its CSS properties in the Styles panel.
5. Temporarily change properties such as "color", "background-color", and "font-size" to observe the changes.
6. Refresh the webpage to restore the original styling saved in the CSS file.

Note: Temporary changes made in DevTools are not automatically saved to "style.css".

Result

The HTML webpage was successfully styled using an external CSS stylesheet. The background, text colors, headings, paragraphs, links, and navigation bar were improved. Chrome DevTools was used to inspect HTML elements and test CSS properties.

Conclusion

This assignment helped me understand how CSS improves the appearance and readability of an HTML webpage. I also learned how to link an external stylesheet and use Chrome DevTools to inspect and modify CSS properties temporarily.

Submission

- "index.html" — HTML webpage linked to the stylesheet.
- "style.css" — External CSS file containing the styling rules.