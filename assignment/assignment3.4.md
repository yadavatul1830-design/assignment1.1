Assignment 3.4 — Semantic HTML Structure

Q1. Structure the page using "<header>", "<nav>", "<main>", "<section>", "<article>", "<aside>", and "<footer>" where appropriate.

Answer: I used semantic HTML elements to organize the webpage into a header, navigation bar, main content, sections, article, sidebar, and footer. These elements make the webpage structure clear and meaningful.

Q2. Keep navigation links inside "<nav>".

Answer: I placed the Home, About, Education, and Contact links inside the "<nav>" element to help users navigate between page sections.

Q3. Keep the main content inside "<main>".

Answer: I placed the primary webpage content inside the "<main>" element, including the About Me, Education, and Mechanical Engineering sections.

Q4. Use the correct heading hierarchy.

Answer: I used "<h1>" for the main heading, "<h2>" for major sections, and "<h3>" for subsections to maintain a proper heading hierarchy.

Q5. Add meaningful alt text for images.

Answer: I used the "alt" attribute in the "<img>" tag to provide meaningful descriptions of images for accessibility and situations where images do not load.

Q6. Check that links and page sections are understandable.

Answer: I opened the webpage in a browser and checked that navigation links worked correctly and that each section had a clear heading and understandable content.

HTML Code — "index.html"

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

    <nav>
        <a href="#home">Home</a> |
        <a href="#about">About</a> |
        <a href="#education">Education</a> |
        <a href="#skills">Skills</a> |
        <a href="#contact">Contact</a>
    </nav>

    <hr>

    <main>
        <section id="about">
            <h2>About Me</h2>
            <p>
                Hello! I am a B.Tech Mechanical Engineering student.
                I am interested in machines, design, manufacturing,
                and learning new engineering technologies.
            </p>

            <img src="images/mechanical-engineering.jpg"
                 alt="Mechanical engineering workshop with machines and tools"
                 width="300"
                 height="200">
        </section>

        <hr>

        <section id="education">
            <h2>Education</h2>
            <article>
                <h3>Bachelor of Technology (B.Tech)</h3>
                <p>Branch: Mechanical Engineering</p>
                <p>Focus: Machine design, manufacturing, and thermodynamics.</p>
            </article>
        </section>

        <hr>

        <section id="skills">
            <h2>Technical Skills</h2>
            <article>
                <h3>Engineering Skills</h3>
                <ul>
                    <li>Engineering Mechanics</li>
                    <li>Basic CAD Design</li>
                    <li>Manufacturing Processes</li>
                    <li>Problem Solving</li>
                </ul>
            </article>
        </section>

        <aside>
            <h2>Areas of Interest</h2>
            <p>Automobile Engineering, Robotics, and Machine Design.</p>
        </aside>

        <hr>

        <section id="contact">
            <h2>Contact Information</h2>
            <p>Email: student@example.com</p>
            <p>Course: B.Tech Mechanical Engineering</p>
        </section>
    </main>

    <footer>
        <p>Thank you for visiting my portfolio.</p>
    </footer>

</body>
</html>

Submission

1. Updated semantic HTML file: "index.html".
2. Before screenshot: Capture the original webpage before applying semantic structure.
3. After screenshot: Capture the updated webpage in a browser after applying the semantic HTML elements.

Note: Replace the sample email with the student's email and ensure that "images/mechanical-engineering.jpg" exists in the "images" folder. If there is no original version, create a simple non-semantic version first to capture the before screenshot.