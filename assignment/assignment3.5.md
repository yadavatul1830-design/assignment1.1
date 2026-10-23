Assignment 3.5 — Blog / Portfolio Mini-Project

Q1. Create a header with name/logo and a navigation bar.

Answer: I created a header displaying my name and a navigation bar with links to Home, About Me, Skills, Projects, and Contact sections.

Q2. Create an About Me section.

Answer: I added an About Me section introducing myself as a B.Tech Mechanical Engineering student interested in machines, design, and manufacturing technology.

Q3. Create sections for skills or interests, blog posts or projects, and images.

Answer: I added a list of technical skills and interests, project descriptions, and images related to mechanical engineering using HTML lists and image tags.

Q4. Add useful links to the website.

Answer: I added useful links to educational and engineering websites. I used the "<a>" tag to make these links clickable.

Q5. Create a footer with contact details and use semantic HTML tags.

Answer: I used semantic tags such as "<header>", "<nav>", "<main>", "<section>", "<article>", and "<footer>" to organize the webpage. The footer contains contact information.

Q6. Ensure navigation links work and the code is clean and properly indented.

Answer: I used working navigation links connected to section IDs, added meaningful image descriptions, and arranged the code with proper indentation. I tested the webpage in a browser.

Source Code

Create a folder named "mechanical-portfolio" with the following structure:

mechanical-portfolio/
├── index.html
└── images/
    ├── workshop.jpg
    └── mechanical-design.jpg

File: "index.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mechanical Engineering Portfolio</title>
</head>
<body>

    <header id="home">
        <h1>My Mechanical Engineering Portfolio</h1>
        <p>B.Tech Mechanical Engineering Student</p>
    </header>

    <hr>

    <nav>
        <a href="#home">Home</a> |
        <a href="#about">About Me</a> |
        <a href="#skills">Skills</a> |
        <a href="#projects">Projects</a> |
        <a href="#links">Useful Links</a> |
        <a href="#contact">Contact</a>
    </nav>

    <hr>

    <main>
        <section id="about">
            <h2>About Me</h2>
            <p>
                Hello! I am a B.Tech Mechanical Engineering student.
                I am interested in machine design, manufacturing,
                automobiles, and modern engineering technologies.
                I enjoy learning new concepts and developing
                practical problem-solving skills.
            </p>
            <img src="images/workshop.jpg"
                 alt="Mechanical engineering workshop with machines and tools"
                 width="300"
                 height="200">
        </section>

        <hr>

        <section id="skills">
            <h2>Skills and Interests</h2>
            <ul>
                <li>Engineering Mechanics</li>
                <li>Basic CAD Design</li>
                <li>Manufacturing Processes</li>
                <li>Problem Solving</li>
                <li>Automobile Engineering</li>
            </ul>
        </section>

        <hr>

        <section id="projects">
            <h2>Projects and Blog Posts</h2>

            <article>
                <h3>Mechanical Design Project</h3>
                <p>
                    This project focuses on understanding basic
                    machine components and their design.
                </p>
                <img src="images/mechanical-design.jpg"
                     alt="Mechanical machine components used for design study"
                     width="300"
                     height="200">
            </article>

            <article>
                <h3>Introduction to Manufacturing</h3>
                <p>
                    This blog post explains basic manufacturing
                    processes such as casting, welding, and machining.
                </p>
            </article>
        </section>

        <hr>

        <section id="links">
            <h2>Useful Links</h2>
            <ul>
                <li>
                    <a href="https://www.asme.org/"
                       target="_blank"
                       rel="noopener noreferrer">
                        ASME — Mechanical Engineering Resources
                    </a>
                </li>
                <li>
                    <a href="https://www.nptel.ac.in/"
                       target="_blank"
                       rel="noopener noreferrer">
                        NPTEL — Engineering Courses
                    </a>
                </li>
            </ul>
        </section>

        <hr>

        <section id="contact">
            <h2>Contact Information</h2>
            <p>Email: student@example.com</p>
            <p>Course: B.Tech Mechanical Engineering</p>
        </section>
    </main>

    <hr>

    <footer>
        <p>Thank you for visiting my portfolio.</p>
        <p>&copy; 2026 Mechanical Engineering Portfolio</p>
    </footer>

</body>
</html>

Git Commands

Run these commands in the terminal from inside the "mechanical-portfolio" folder:

git init
git add .
git commit -m "Create mechanical engineering portfolio"

Create a new repository on GitHub, then connect and push your project using the repository URL provided by GitHub:

git branch -M main
git remote add origin YOUR_GITHUB_REPOSITORY_URL
git push -u origin main

Replace "YOUR_GITHUB_REPOSITORY_URL" with your actual repository URL.

Submission

1. Complete portfolio project folder.
2. "index.html" source code and the "images" folder.
3. Screenshot of the working portfolio in a browser.
4. GitHub repository link after uploading the project.

Note: Add actual image files to the "images" folder and replace "student@example.com" with your friend's email. The GitHub link should be the real URL of the repository after the code has been pushed.