Assignment 2.4: HTML Debugging and Validation

Q1. Take a sample HTML file containing missing closing tags, incorrect nesting, and missing attributes.

Answer: I created a sample HTML file containing common errors such as missing closing tags, incorrect nesting of elements, and missing attributes.

Q2. Identify the errors.

Answer: The following errors were identified:

- Missing closing tags for HTML elements.
- Incorrect nesting of elements.
- Missing "alt" attribute in the image tag.
- Improper indentation of the code.

Q3. Inspect using the Elements panel in browser DevTools.

Answer: I opened the webpage in a browser and used the Elements panel in Developer Tools to inspect the HTML structure and identify errors.

Q4. Check the markup using an HTML validation tool.

Answer: I used the "W3C Markup Validation Service" (https://validator.w3.org/) to check the HTML code and identify markup errors.

Q5. Fix all errors and properly indent the code.

Answer: I corrected the missing closing tags, fixed the nesting, added the missing attributes, and properly indented the code.

Submission: Before-and-After HTML Code

Before (Incorrect HTML Code)

<!DOCTYPE html>
<html>
<head>
    <title>My Webpage</title>
<body>
    <h1>Welcome to My Webpage
    <p>This is my introduction.
    <div>
        <p>My hobbies are:
        <ul>
            <li>Reading
            <li>Learning
        </ul>
    </div>
    <img src="photo.jpg">
</body>
</html>

After (Corrected HTML Code)

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Webpage</title>
</head>
<body>
    <h1>Welcome to My Webpage</h1>

    <p>This is my introduction.</p>

    <div>
        <p>My hobbies are:</p>
        <ul>
            <li>Reading</li>
            <li>Learning</li>
        </ul>
    </div>

    <img src="photo.jpg" alt="A personal photograph">
</body>
</html>

Screenshot submission: Open the corrected HTML file in a browser and take a screenshot of the fixed webpage. You can also take a screenshot of the validation result after checking the corrected code with the W3C validator.