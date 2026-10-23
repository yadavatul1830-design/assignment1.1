Assignment 3.3 — College Information Webpage

Q1. Write an introduction for the college/course.

Answer: I created an introduction section for my college and the Bachelor of Technology (B.Tech) in Mechanical Engineering course using HTML headings and paragraphs.

Q2. Make a list of departments or subjects using "<ul>".

Answer: I used the "<ul>" tag to display a list of engineering departments and mechanical engineering subjects in bullet-point format.

Q3. Show the admission process using "<ol>".

Answer: I used the "<ol>" tag to display the admission process in a numbered sequence of steps.

Q4. Arrange topics of any subject in a nested list.

Answer: I created a nested list to organize Mechanical Engineering subjects and their related topics using HTML list elements.

Q5. Use "<dl>", "<dt>", and "<dd>" for details of teachers or courses.

Answer: I used "<dl>" to create a description list, "<dt>" for course or subject names, and "<dd>" to provide their descriptions.

Q6. Organize the page through headings and sections.

Answer: I used HTML headings and "<section>" elements to organize the webpage into different sections, making the information clear and easy to understand.

HTML Code — "college-info.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mechanical Engineering College Information</title>
</head>
<body>

    <header>
        <h1>College Information</h1>
        <h2>B.Tech in Mechanical Engineering</h2>
        <p>Welcome to the Mechanical Engineering Information Page.</p>
    </header>

    <hr>

    <section>
        <h2>Introduction</h2>
        <p>
            Mechanical Engineering is an engineering field that deals
            with the design, manufacturing, operation, and maintenance
            of machines and mechanical systems. The B.Tech course
            provides students with technical knowledge and practical skills.
        </p>
    </section>

    <hr>

    <section>
        <h2>Engineering Departments</h2>
        <ul>
            <li>Mechanical Engineering</li>
            <li>Civil Engineering</li>
            <li>Computer Science Engineering</li>
            <li>Electrical Engineering</li>
            <li>Electronics and Communication Engineering</li>
        </ul>
    </section>

    <hr>

    <section>
        <h2>Admission Process</h2>
        <ol>
            <li>Choose the B.Tech Mechanical Engineering course.</li>
            <li>Check the eligibility requirements.</li>
            <li>Complete the application or entrance examination process.</li>
            <li>Submit the required documents.</li>
            <li>Complete counselling and admission formalities as applicable.</li>
        </ol>
    </section>

    <hr>

    <section>
        <h2>Mechanical Engineering Subjects and Topics</h2>
        <ul>
            <li>Thermodynamics
                <ul>
                    <li>Laws of Thermodynamics</li>
                    <li>Heat and Work</li>
                </ul>
            </li>
            <li>Engineering Mechanics
                <ul>
                    <li>Force and Motion</li>
                    <li>Statics and Dynamics</li>
                </ul>
            </li>
            <li>Manufacturing Technology
                <ul>
                    <li>Welding</li>
                    <li>Casting and Machining</li>
                </ul>
            </li>
            <li>Fluid Mechanics
                <ul>
                    <li>Fluid Pressure</li>
                    <li>Fluid Flow</li>
                </ul>
            </li>
        </ul>
    </section>

    <hr>

    <section>
        <h2>Course Details</h2>
        <dl>
            <dt><strong>B.Tech Mechanical Engineering</strong></dt>
            <dd>An undergraduate engineering course focused on machines, design, manufacturing, and mechanical systems.</dd>

            <dt><strong>Thermodynamics</strong></dt>
            <dd>The study of heat, energy, temperature, and work.</dd>

            <dt><strong>Engineering Mechanics</strong></dt>
            <dd>The study of forces and their effects on objects.</dd>

            <dt><strong>Manufacturing Technology</strong></dt>
            <dd>The study of processes used to manufacture products and machine components.</dd>
        </dl>
    </section>

    <hr>

    <footer>
        <p>Thank you for visiting the College Information Page.</p>
    </footer>

</body>
</html>

Submission

1. "college-info.html" — Completed HTML file.
2. Screenshot of the webpage opened in a browser.