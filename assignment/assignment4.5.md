Assignment 4.5 — Multi-Page College Club Website

Q1. How do you create a home page for a college club?

Answer: The home page introduces the club, explains its purpose, and displays its main activities.

File: "index.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home | College Tech Club</title>
    <meta name="description" content="Welcome to the College Tech Club website.">
    <link rel="icon" type="image/png" href="favicon.png">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>College Tech Club</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="about.html">About</a>
            <a href="registration.html">Registration</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>

    <main>
        <h2>Welcome to Our Club!</h2>
        <p>Our club helps students learn technology, develop skills,
        and work together on creative projects.</p>

        <h3>Our Activities</h3>
        <ul>
            <li>Technical workshops</li>
            <li>Project competitions</li>
            <li>Guest lectures</li>
            <li>Team activities</li>
        </ul>

        <h3>Upcoming Events</h3>
        <table>
            <caption>Club Events Schedule</caption>
            <thead>
                <tr>
                    <th>Event</th>
                    <th>Date</th>
                    <th>Venue</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Web Design Workshop</td>
                    <td>10 November</td>
                    <td>Computer Lab</td>
                </tr>
                <tr>
                    <td>Project Competition</td>
                    <td>18 November</td>
                    <td>Seminar Hall</td>
                </tr>
                <tr>
                    <td>Guest Lecture</td>
                    <td>25 November</td>
                    <td>Auditorium</td>
                </tr>
            </tbody>
        </table>
    </main>

    <footer>
        <p>&copy; 2026 College Tech Club</p>
    </footer>
</body>
</html>

Q2. How do you create an About page with club details and member information?

Answer: The About page explains the club's mission, goals, and members.

File: "about.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About | College Tech Club</title>
    <meta name="description" content="Learn about our club, its goals, and members.">
    <link rel="icon" type="image/png" href="favicon.png">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>About Our Club</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="about.html">About</a>
            <a href="registration.html">Registration</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>

    <main>
        <h2>Who We Are</h2>
        <p>The College Tech Club is a student organization that
        encourages technical learning, creativity, and teamwork.</p>

        <h2>Our Mission</h2>
        <p>Our mission is to help students improve their knowledge
        and practical skills through workshops and projects.</p>

        <h2>Club Members</h2>
        <ul>
            <li>Faculty Coordinator: Mr. Amit Sharma</li>
            <li>President: Rahul Verma</li>
            <li>Secretary: Priya Singh</li>
            <li>Event Coordinator: Aman Kumar</li>
        </ul>
    </main>

    <footer>
        <p>&copy; 2026 College Tech Club</p>
    </footer>
</body>
</html>

Q3. How do you create a student registration form?

Answer: A registration form collects student details such as name, email, course, and interests.

File: "registration.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration | College Tech Club</title>
    <meta name="description" content="Register to become a member of the College Tech Club.">
    <link rel="icon" type="image/png" href="favicon.png">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Club Registration</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="about.html">About</a>
            <a href="registration.html">Registration</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>

    <main>
        <h2>Join Our Club</h2>

        <form action="#" method="post">
            <label for="name">Full Name:</label>
            <input type="text" id="name" name="name" required>
            <br><br>

            <label for="email">Email Address:</label>
            <input type="email" id="email" name="email" required>
            <br><br>

            <label for="phone">Phone Number:</label>
            <input type="tel" id="phone" name="phone" required>
            <br><br>

            <label for="course">Course:</label>
            <select id="course" name="course" required>
                <option value="">Select your course</option>
                <option value="BTech">B.Tech</option>
                <option value="BBA">BBA</option>
                <option value="BCA">BCA</option>
                <option value="Other">Other</option>
            </select>
            <br><br>

            <p>Choose your interests:</p>
            <input type="checkbox" id="coding" name="interest" value="Coding">
            <label for="coding">Coding</label>

            <input type="checkbox" id="design" name="interest" value="Design">
            <label for="design">Web Design</label>

            <input type="checkbox" id="events" name="interest" value="Events">
            <label for="events">Event Management</label>
            <br><br>

            <label for="reason">Why do you want to join?</label>
            <br>
            <textarea id="reason" name="reason" rows="4" required></textarea>
            <br><br>

            <button type="submit">Submit Registration</button>
        </form>
    </main>

    <footer>
        <p>&copy; 2026 College Tech Club</p>
    </footer>
</body>
</html>

Q4. How do you create a Contact page?

Answer: The Contact page provides the club's email address, location, and contact information.

File: "contact.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact | College Tech Club</title>
    <meta name="description" content="Contact the College Tech Club for information and queries.">
    <link rel="icon" type="image/png" href="favicon.png">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Contact Us</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="about.html">About</a>
            <a href="registration.html">Registration</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>

    <main>
        <h2>Get in Touch</h2>
        <p><strong>Email:</strong>
            <a href="mailto:techclub@example.com">techclub@example.com</a>
        </p>
        <p><strong>Location:</strong> College Campus, Student Activity Centre</p>
        <p><strong>Contact Person:</strong> Club Coordinator</p>
        <p><strong>Office Hours:</strong> Monday to Friday, 10 AM to 4 PM</p>
    </main>

    <footer>
        <p>&copy; 2026 College Tech Club</p>
    </footer>
</body>
</html>

Q5. How do you maintain consistent navigation across all four pages?

Answer: Add the same navigation links to every page. Each link uses the correct HTML filename so users can move between Home, About, Registration, and Contact.

Example:

<nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="registration.html">Registration</a>
    <a href="contact.html">Contact</a>
</nav>

Q6. How do you add an information table, such as an events schedule?

Answer: Use the "<table>", "<caption>", "<thead>", "<tbody>", "<tr>", "<th>", and "<td>" tags to display events, dates, and venues in an organized format. The events schedule is included on the home page.

Q7. How do you add metadata, a favicon, and CSS to each page?

Answer: Add UTF-8 encoding, a viewport tag, a meaningful title, a meta description, a favicon link, and a stylesheet link inside the "<head>" section of every page.

Example:

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Home | College Tech Club</title>
<meta name="description" content="Official website of the College Tech Club.">
<link rel="icon" type="image/png" href="favicon.png">
<link rel="stylesheet" href="style.css">

Q8. How do you test all internal links?

Answer: Open "index.html" in a browser and click every navigation link. Check that each page opens correctly and that the registration form and event table display properly. Also check that the CSS and favicon load without errors.

---

Additional File: "style.css"

Create a file named "style.css" in the same folder as all four HTML files.

body {
    font-family: Arial, sans-serif;
    margin: 0;
    background-color: #f4f7fb;
    color: #222;
    line-height: 1.6;
}

header {
    background-color: #24476b;
    color: white;
    text-align: center;
    padding: 20px;
}

nav a {
    color: white;
    text-decoration: none;
    margin: 0 10px;
    font-weight: bold;
}

nav a:hover {
    text-decoration: underline;
}

main {
    padding: 25px;
    max-width: 900px;
    margin: auto;
    background-color: white;
}

table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 15px;
}

caption {
    font-weight: bold;
    padding: 10px;
}

th, td {
    border: 1px solid #999;
    padding: 10px;
    text-align: left;
}

th {
    background-color: #dbeafe;
}

input, select, textarea {
    padding: 8px;
    max-width: 100%;
}

footer {
    background-color: #24476b;
    color: white;
    text-align: center;
    padding: 12px;
    margin-top: 20px;
}

button {
    padding: 10px 16px;
    background-color: #24476b;
    color: white;
    border: none;
    cursor: pointer;
}

@media (max-width: 600px) {
    nav a {
        display: inline-block;
        margin: 5px;
    }

    main {
        padding: 15px;
    }
}

Folder Structure

Keep all files in one folder:

College-Club-Website/
├── index.html
├── about.html
├── registration.html
├── contact.html
├── style.css
└── favicon.png

Submission checklist:

1. Save all four HTML files and "style.css".
2. Add a real icon image named "favicon.png" to the folder.
3. Open "index.html" in your browser.
4. Test all navigation links and check the registration form.
5. Take a screenshot of the website and submit it with "Assignment-4.5.md".