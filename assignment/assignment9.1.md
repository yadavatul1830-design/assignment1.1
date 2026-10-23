Assignment 9.1 — Convert a Desktop Page into a Mobile-First Layout

Q1. What is a responsive webpage?

Answer: A responsive webpage automatically adjusts its layout according to the screen size of a mobile phone, tablet, or desktop computer.

Q2. How do you verify the viewport meta tag in HTML?

Answer: The viewport meta tag helps the webpage fit the device screen properly. Add this tag inside the "<head>" section.

<meta name="viewport" content="width=device-width, initial-scale=1.0">

Q3. How do you write CSS for mobile screens first?

Answer: Mobile-first design means writing the basic CSS for smaller screens first and then improving the layout for larger screens.

.container {
    display: grid;
    grid-template-columns: 1fr;
    gap: 15px;
    padding: 15px;
}

This code displays one column on mobile screens.

Q4. How do you improve the layout for tablets and desktops using media queries?

Answer: Media queries apply different CSS rules depending on the screen width.

/* Tablet */
@media (min-width: 600px) {
    .container {
        grid-template-columns: repeat(2, 1fr);
    }
}

/* Desktop */
@media (min-width: 1024px) {
    .container {
        grid-template-columns: repeat(3, 1fr);
    }
}

Q5. What are breakpoints? Give at least two examples.

Answer: Breakpoints are screen widths at which the webpage layout changes to fit the device.

- 600px: Changes the layout for tablets.
- 1024px: Changes the layout for desktops.

These are example breakpoints and can be adjusted according to the design.

Q6. How do you test a responsive webpage using Chrome DevTools?

Answer:

1. Open the webpage in Google Chrome.
2. Right-click the page and select Inspect.
3. Click the Toggle Device Toolbar icon.
4. Select a mobile, tablet, or desktop device.
5. Check whether the content fits the screen correctly.
6. Adjust the screen width to test different sizes.

Q7. How do you fix horizontal overflow and overlapping elements?

Answer: Use flexible widths, responsive images, and suitable spacing to prevent elements from going outside the screen.

* {
    box-sizing: border-box;
}

img {
    max-width: 100%;
    height: auto;
}

body {
    margin: 0;
    overflow-wrap: anywhere;
}

.container {
    width: 100%;
    max-width: 1200px;
    margin: auto;
}

These rules help prevent horizontal scrolling and make content fit smaller screens.

---

Practical Implementation

Create two files: "index.html" and "style.css".

File 1: "index.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Student Dashboard</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="header">
        <h1>Student Dashboard</h1>
        <p>Welcome to your learning dashboard</p>
    </header>

    <nav class="navigation">
        <a href="#home">Home</a>
        <a href="#courses">Courses</a>
        <a href="#tasks">Tasks</a>
        <a href="#profile">Profile</a>
    </nav>

    <main class="container" id="home">
        <section class="card">
            <h2>My Courses</h2>
            <p>HTML and CSS</p>
            <p>JavaScript Basics</p>
        </section>

        <section class="card" id="tasks">
            <h2>Pending Tasks</h2>
            <p>Complete HTML Assignment</p>
            <p>Submit CSS Project</p>
        </section>

        <section class="card" id="profile">
            <h2>My Profile</h2>
            <p>Name: Student</p>
            <p>Course: B.Tech</p>
        </section>

        <section class="card" id="courses">
            <h2>Announcements</h2>
            <p>Next workshop: Web Design</p>
            <p>Check your assignment deadlines.</p>
        </section>
    </main>

    <footer class="footer">
        <p>&copy; 2026 Student Dashboard</p>
    </footer>

</body>
</html>

File 2: "style.css"

/* Common settings */
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-color: #f1f5f9;
    color: #222;
    overflow-wrap: anywhere;
}

/* Header */
.header {
    background-color: #24476b;
    color: white;
    text-align: center;
    padding: 20px 15px;
}

/* Navigation */
.navigation {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
    background-color: #18334f;
    padding: 12px;
}

.navigation a {
    color: white;
    text-decoration: none;
    padding: 8px;
}

/* Mobile-first layout */
.container {
    display: grid;
    grid-template-columns: 1fr;
    gap: 15px;
    padding: 15px;
    width: 100%;
    max-width: 1200px;
    margin: auto;
}

.card {
    background-color: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 5px #cccccc;
    min-width: 0;
}

.footer {
    background-color: #24476b;
    color: white;
    text-align: center;
    padding: 12px;
}

/* Tablet breakpoint */
@media (min-width: 600px) {
    .container {
        grid-template-columns: repeat(2, minmax(0, 1fr));
        padding: 20px;
    }

    .header {
        padding: 30px;
    }
}

/* Desktop breakpoint */
@media (min-width: 1024px) {
    .container {
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 20px;
        padding: 25px;
    }
}

Submission Checklist

- Save the assignment as "Assignment-9.1.md".
- Save the webpage as "index.html".
- Save the responsive styles as "style.css".
- Open "index.html" in Chrome and test the mobile, tablet, and desktop layouts using Device Mode.
- Take three screenshots showing the page at mobile, tablet, and desktop sizes.
- Submit the updated HTML/CSS files and all three screenshots.