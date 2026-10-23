Assignment 3.2 — Images in HTML

Q1. Create a folder named "images" in your project.

Answer: I created a folder named "images" inside my project folder to store all the images used on my portfolio webpage.

Q2. Add at least 3 images.

Answer: I added three images to the "images" folder to display my profile, education, and hobbies on my portfolio page.

Q3. Use "src", "alt", "width", and "height" in the "<img>" tag.

Answer: I used the "src" attribute to specify the image path, "alt" to describe the image, and "width" and "height" to set its dimensions.

Q4. Keep image paths correct.

Answer: I used relative paths such as "images/profile.jpg" to connect the images folder with my HTML file.

Q5. Write meaningful alt text for each image.

Answer: I added meaningful alternative text to each image so users can understand the image content if it does not load or if they use a screen reader.

Q6. Check that images are loading properly in the browser.

Answer: I opened my portfolio page in a web browser and checked that all three images were displayed correctly.

HTML Code — "index.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
</head>
<body>

    <header>
        <h1>Radhika Singh's Portfolio</h1>
        <p>Welcome to my personal portfolio webpage.</p>
    </header>

    <hr>

    <section>
        <h2>About Me</h2>
        <p>Hello! I am Radhika Singh, a BBA student
        interested in learning new skills.</p>

        <img src="images/profile.jpg"
             alt="Profile photograph of Radhika Singh"
             width="200"
             height="200">
    </section>

    <hr>

    <section>
        <h2>Education</h2>
        <p>I am pursuing my Bachelor of Business Administration
        from Invertis University.</p>

        <img src="images/education.jpg"
             alt="Books and study materials representing education"
             width="300"
             height="200">
    </section>

    <hr>

    <section>
        <h2>Hobbies</h2>
        <p>I enjoy reading books and learning new things.</p>

        <img src="images/hobbies.jpg"
             alt="Books representing my hobby of reading"
             width="300"
             height="200">
    </section>

</body>
</html>

Project Folder Structure

my-portfolio/
│
├── index.html
│
└── images/
    ├── profile.jpg
    ├── education.jpg
    └── hobbies.jpg

Submission

1. "index.html" — Portfolio webpage.
2. "images" folder containing at least three images.

Note: Add your actual image files to the "images" folder and ensure their names and extensions match the paths in your HTML code. Then open "index.html" in a browser to verify that all images load correctly.