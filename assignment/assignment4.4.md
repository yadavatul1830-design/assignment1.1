Assignment 4.4 — Metadata & Page Setup

Q1. How do you set UTF-8 character encoding in every HTML file?

Answer: We use the following meta tag inside the "<head>" section to support letters, numbers, and special characters correctly.

<meta charset="UTF-8">

Q2. How do you add a mobile viewport meta tag?

Answer: The viewport meta tag helps a webpage adjust to different screen sizes, especially mobile phones.

<meta name="viewport" content="width=device-width, initial-scale=1.0">

Q3. How do you write a meaningful title for each page?

Answer: The "<title>" tag gives a meaningful name to the webpage. It appears on the browser tab.

<title>Student Marksheet</title>

Q4. How do you add a meta description?

Answer: A meta description gives a short summary of the webpage. Search engines may use it in search results.

<meta name="description" content="A student marksheet showing marks in HTML, CSS, and JavaScript.">

Q5. How do you add a favicon?

Answer: A favicon is a small icon displayed on the browser tab. Save an icon image as "favicon.png" in the same folder as the HTML file, then add this code inside "<head>".

<link rel="icon" type="image/png" href="favicon.png">

Q6. How do you verify CSS links and file paths?

Answer: We should check that the CSS and favicon files exist at the specified locations. For example, if the CSS file is inside a folder named "css", use:

<link rel="stylesheet" href="css/style.css">

If the CSS file is in the same folder as the HTML file, use:

<link rel="stylesheet" href="style.css">

We can also open the webpage in a browser and use Developer Tools to check for missing files or errors.

---

Metadata Code

Add the following metadata to the "<head>" section of your existing HTML projects.

Example: "marksheet.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Student Marksheet</title>

    <meta name="description"
          content="A student marksheet showing marks and total scores for five students.">

    <link rel="icon" type="image/png" href="favicon.png">
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <h1>Student Marksheet</h1>
    <p>This page displays student marks in a table.</p>

</body>
</html>

Note: Keep your existing webpage content inside the "<body>" section. The example above shows where the metadata belongs.

Submission

1. Update the "<head>" section of each old HTML project.
2. Save the changes in the respective HTML files.
3. Check that the CSS and favicon paths are correct.
4. Open the updated webpage in a browser.
5. Take a screenshot showing the webpage and its favicon on the browser tab.
6. Submit the updated HTML files and the metadata code.