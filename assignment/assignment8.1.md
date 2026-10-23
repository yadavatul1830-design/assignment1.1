Assignment 8.1 — Dashboard-Style Grid Layout

Q1. What is a dashboard-style layout?

Answer: A dashboard is a webpage that displays important information in one place. It can contain a header, sidebar, statistic cards, and other useful details. CSS Grid helps arrange these elements neatly.

Q2. Create a dashboard header.

Answer: The header displays the dashboard title and a welcome message. We can create it using the HTML "<header>" tag.

<header class="header">
    <h1>Student Dashboard</h1>
    <p>Welcome to your dashboard!</p>
</header>

Q3. Create a sidebar and main content area.

Answer: The sidebar contains navigation links, while the main content area displays the dashboard information.

<aside class="sidebar">
    <h2>Menu</h2>
    <a href="#">Dashboard</a>
    <a href="#">My Courses</a>
    <a href="#">Assignments</a>
    <a href="#">Results</a>
</aside>

<main class="main-content">
    <h2>Dashboard Overview</h2>
    <p>Here is your academic summary.</p>
</main>

Q4. Add three or four statistic cards to the dashboard.

Answer: Statistic cards display important information such as enrolled courses, completed assignments, upcoming tasks, and attendance.

<div class="stats">
    <div class="card">
        <h3>Courses</h3>
        <p>6 Enrolled</p>
    </div>

    <div class="card">
        <h3>Assignments</h3>
        <p>12 Completed</p>
    </div>

    <div class="card">
        <h3>Upcoming Tasks</h3>
        <p>4 Pending</p>
    </div>

    <div class="card">
        <h3>Attendance</h3>
        <p>92%</p>
    </div>
</div>

Q5. How is CSS Grid used in the outer layout?

Answer: CSS Grid arranges the header, sidebar, and main content area into rows and columns. The "display: grid" property enables Grid layout.

.dashboard {
    display: grid;
    grid-template-columns: 220px 1fr;
    grid-template-rows: 80px 1fr;
    min-height: 100vh;
}

Here, "220px" sets the sidebar width, and "1fr" allows the main content to use the remaining space.

Q6. How do grid-template-columns, grid-template-rows, and gap work?

Answer:

- "grid-template-columns" sets the width of the columns.
- "grid-template-rows" sets the height of the rows.
- "gap" adds space between grid items.

Example:

.stats {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
}

This creates two equal-width columns with 20 pixels of space between the cards.

Q7. Create and inspect the complete dashboard webpage.

Answer: The following code combines the header, sidebar, main content area, and four statistic cards.

File 1: "index.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Dashboard</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="dashboard">

        <header class="header">
            <h1>Student Dashboard</h1>
            <p>Welcome to your dashboard!</p>
        </header>

        <aside class="sidebar">
            <h2>Menu</h2>
            <a href="#">Dashboard</a>
            <a href="#">My Courses</a>
            <a href="#">Assignments</a>
            <a href="#">Results</a>
            <a href="#">Settings</a>
        </aside>

        <main class="main-content">
            <h2>Dashboard Overview</h2>
            <p>Here is your academic summary.</p>

            <section class="stats">
                <div class="card">
                    <h3>Courses</h3>
                    <p>6 Enrolled</p>
                </div>

                <div class="card">
                    <h3>Assignments</h3>
                    <p>12 Completed</p>
                </div>

                <div class="card">
                    <h3>Upcoming Tasks</h3>
                    <p>4 Pending</p>
                </div>

                <div class="card">
                    <h3>Attendance</h3>
                    <p>92%</p>
                </div>
            </section>
        </main>

    </div>

</body>
</html>

File 2: "style.css"

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f1f5f9;
    color: #1e293b;
}

.dashboard {
    display: grid;
    grid-template-columns: 220px 1fr;
    grid-template-rows: 80px 1fr;
    min-height: 100vh;
}

.header {
    grid-column: 1 / 3;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #1d4ed8;
    color: white;
    padding: 20px;
}

.sidebar {
    background-color: white;
    padding: 25px 15px;
    border-right: 1px solid #e2e8f0;
}

.sidebar h2 {
    margin-bottom: 20px;
}

.sidebar a {
    display: block;
    text-decoration: none;
    color: #334155;
    padding: 12px;
    margin-bottom: 8px;
    border-radius: 6px;
}

.sidebar a:hover {
    background-color: #dbeafe;
    color: #1d4ed8;
}

.main-content {
    padding: 30px;
    min-width: 0;
}

.main-content h2 {
    margin-bottom: 10px;
}

.main-content > p {
    margin-bottom: 25px;
    color: #64748b;
}

.stats {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 20px;
}

.card {
    background-color: white;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
    border-left: 4px solid #2563eb;
}

.card h3 {
    margin-bottom: 12px;
    color: #475569;
}

.card p {
    font-size: 24px;
    font-weight: bold;
    color: #1d4ed8;
}

@media (max-width: 600px) {
    .dashboard {
        grid-template-columns: 1fr;
        grid-template-rows: auto auto 1fr;
    }

    .header {
        grid-column: 1;
        flex-direction: column;
        align-items: flex-start;
        gap: 10px;
    }

    .sidebar {
        border-right: none;
        border-bottom: 1px solid #e2e8f0;
    }

    .main-content {
        padding: 20px;
    }

    .stats {
        grid-template-columns: 1fr;
    }
}

Steps to inspect the Grid layout

1. Save both files in the same folder.
2. Open "index.html" in a web browser.
3. Right-click the webpage and select Inspect.
4. Open the Elements panel and select the ".dashboard" or ".stats" element.
5. Inspect "display: grid", "grid-template-columns", "grid-template-rows", and "gap" in the Styles panel.
6. Resize the browser window to see how the dashboard adjusts to a smaller screen.

Result

A dashboard webpage is created using CSS Grid. It contains a header, sidebar, main content area, and four statistic cards. Grid rows, columns, and gaps organize the content neatly, while a media query makes the layout responsive.

Submission

- "index.html" — Dashboard webpage
- "style.css" — CSS styling file
- Screenshot of the completed dashboard in a browser