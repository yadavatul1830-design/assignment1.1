Assignment 2.3: HTML Page Structure and Attributes

Q1. Divide the page into Header, About, Education, Skills, and Contact sections.

Answer: I divided the webpage into five sections: Header, About, Education, Skills, and Contact to organize the content properly.

Q2. Use div for containers.

Answer: I used the "<div>" tag to group related content into separate containers for better organization.

Q3. Give elements unique id and reusable class attributes.

Answer: I used unique "id" attributes to identify specific elements and reusable "class" attributes to group similar elements.

Q4. Add a data- custom attribute to any element.*

Answer: I added a custom "data-*" attribute to an HTML element to store additional information.

Q5. Update a text element and add new content.

Answer: I updated the introduction paragraph and added new content about my interests, skills, and career goals.

Q6. Organize the HTML code with proper indentation and meaningful names.

Answer: I used proper indentation, meaningful IDs, and descriptive class names to make the HTML code easy to read and understand.

Submission: Updated HTML File

Save the following code as "index.html".

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Personal Webpage</title>
</head>
<body>

    <!-- Header Section -->
    <div id="header" class="section">
        <h1>Atul Yadav</h1>
        <p>Welcome to My Personal Webpage</p>
    </div>

    <hr>

    <!-- About Section -->
    <div id="about" class="section">
        <h2>About Me</h2>
        <p data-info="introduction">
            Hello! I am Atul Yadav, a B.Tech student at Invertis University.
            I enjoy learning new skills and exploring business and management.
            My goal is to develop my professional and communication skills.
        </p>
    </div>

    <hr>

    <!-- Education Section -->
    <div id="education" class="section">
        <h2>Education</h2>
        <p class="details">
            I am pursuing a B.Tech (B.Tech)
            from Invertis University.
        </p>
    </div>

    <hr>

    <!-- Skills Section -->
    <div id="skills" class="section">
        <h2>My Skills</h2>
        <p class="details">
            Communication, Teamwork, Leadership,
            Problem Solving, and Time Management.
        </p>
    </div>

    <hr>

    <!-- Contact Section -->
    <div id="contact" class="section">
        <h2>Contact</h2>
        <p class="details">
            Thank you for visiting my webpage.
        </p>
    </div>

</body>
</html>

Screenshot submission: Open "index.html" in a web browser and take a screenshot showing the complete webpage structure.