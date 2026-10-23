Assignment 8.3 — Magazine Layout Using Grid Areas

Q1. What is a magazine-style webpage?

Answer: A magazine-style webpage is used to display news articles, stories, and other information in an organized layout. It usually contains a header, navigation bar, main article, sidebar, and footer. CSS Grid helps arrange these sections neatly.

Q2. Create the header, navigation, main article, sidebar, and footer sections.

Answer: We use HTML semantic tags to create different sections of the webpage.

- "<header>" displays the website title.
- "<nav>" contains navigation links.
- "<main>" contains the main article.
- "<aside>" displays additional news or related information.
- "<footer>" displays copyright information.

Example:

<header class="header">Daily News</header>
<nav class="navigation">Home | World | Sports | Technology</nav>
<main class="article">Main News Article</main>
<aside class="sidebar">Related News</aside>
<footer class="footer">Copyright Information</footer>

Q3. How do we define a Grid container?

Answer: A Grid container is created by applying "display: grid" to an HTML element. It allows us to arrange webpage sections in rows and columns.

Example:

.magazine {
    display: grid;
    gap: 15px;
    padding: 20px;
}

Here, "display: grid" enables CSS Grid, while "gap" creates space between the sections.

Q4. What is "grid-template-areas"?

Answer: The "grid-template-areas" property allows us to design a layout by giving names to different grid sections. It makes the CSS layout easy to understand and manage.

Example:

.magazine {
    display: grid;
    grid-template-areas:
        "header header"
        "nav nav"
        "article sidebar"
        "footer footer";
    grid-template-columns: 2fr 1fr;
    gap: 15px;
}

In this example, the main article gets twice as much column space as the sidebar. The header, navigation, and footer occupy the full width.

Q5. How do we assign named grid areas to each section?

Answer: We use the "grid-area" property to assign each section to its named area.

Example:

.header {
    grid-area: header;
}

.navigation {
    grid-area: nav;
}

.article {
    grid-area: article;
}

.sidebar {
    grid-area: sidebar;
}

.footer {
    grid-area: footer;
}

This places each section in the correct position according to "grid-template-areas".

Q6. Create and test the complete magazine-style webpage.

Answer: The following code creates a complete news-style webpage using CSS Grid areas. Save the two files in the same folder.

File 1: "index.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Daily News Magazine</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="magazine">

        <header class="header">
            <h1>Daily News</h1>
            <p>Your source for the latest updates</p>
        </header>

        <nav class="navigation">
            <a href="#">Home</a>
            <a href="#">World</a>
            <a href="#">Technology</a>
            <a href="#">Sports</a>
            <a href="#">Entertainment</a>
        </nav>

        <main class="article">
            <h2>Technology Is Changing the World</h2>
            <p class="date">Published: October 2026</p>

            <img
                src="https://images.unsplash.com/photo-1518770660439-4636190af475?auto=format&fit=crop&w=1000&q=80"
                alt="Electronic technology circuit board">

            <p>
                Technology has become an important part of our daily lives.
                It has changed the way people communicate, study, work, and
                share information.
            </p>

            <p>
                Modern innovations such as artificial intelligence,
                smartphones, and digital platforms are creating new
                opportunities in education, business, and healthcare.
            </p>

            <p>
                As technology continues to develop, people must learn new
                skills and use digital tools responsibly.
            </p>
        </main>

        <aside class="sidebar">
            <h2>Related News</h2>

            <div class="news-item">
                <h3>Education</h3>
                <p>Online learning is making education more accessible.</p>
            </div>

            <div class="news-item">
                <h3>Business</h3>
                <p>Digital tools are helping businesses reach new customers.</p>
            </div>

            <div class="news-item">
                <h3>Science</h3>
                <p>Researchers continue to explore new technologies.</p>
            </div>
        </aside>

        <footer class="footer">
            <p>&copy; 2026 Daily News Magazine. All rights reserved.</p>
        </footer>

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
    line-height: 1.6;
}

.magazine {
    display: grid;
    grid-template-areas:
        "header header"
        "nav nav"
        "article sidebar"
        "footer footer";
    grid-template-columns: 2fr 1fr;
    gap: 20px;
    max-width: 1200px;
    margin: 20px auto;
    padding: 20px;
}

.header {
    grid-area: header;
    background-color: #1e3a8a;
    color: white;
    text-align: center;
    padding: 30px;
}

.navigation {
    grid-area: nav;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 25px;
    background-color: #2563eb;
    padding: 15px;
}

.navigation a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

.navigation a:hover {
    text-decoration: underline;
}

.article {
    grid-area: article;
    background-color: white;
    padding: 25px;
    border-radius: 8px;
}

.article h2 {
    margin-bottom: 8px;
    color: #1e3a8a;
}

.date {
    color: #64748b;
    font-size: 14px;
    margin-bottom: 15px;
}

.article img {
    width: 100%;
    height: 280px;
    object-fit: cover;
    border-radius: 8px;
    margin-bottom: 15px;
}

.article p {
    margin-bottom: 15px;
}

.sidebar {
    grid-area: sidebar;
    background-color: white;
    padding: 25px;
    border-radius: 8px;
}

.sidebar h2 {
    color: #1e3a8a;
    margin-bottom: 15px;
}

.news-item {
    border-bottom: 1px solid #e2e8f0;
    padding: 15px 0;
}

.news-item:last-child {
    border-bottom: none;
}

.news-item h3 {
    margin-bottom: 5px;
}

.footer {
    grid-area: footer;
    background-color: #1e293b;
    color: white;
    text-align: center;
    padding: 20px;
}

/* Responsive layout for mobile devices */
@media (max-width: 650px) {
    .magazine {
        grid-template-areas:
            "header"
            "nav"
            "article"
            "sidebar"
            "footer";
        grid-template-columns: 1fr;
        padding: 12px;
        gap: 12px;
        margin: 0 auto;
    }

    .header {
        padding: 20px;
    }

    .navigation {
        gap: 12px;
    }

    .article,
    .sidebar {
        padding: 18px;
    }

    .article img {
        height: 200px;
    }
}

Testing the layout

1. Save the files as "index.html" and "style.css" in the same folder.
2. Open "index.html" in a web browser.
3. Check that the header and navigation span the full width.
4. Verify that the main article is wider than the sidebar.
5. Resize the browser window or use Developer Tools to test the mobile layout.
6. Change "grid-template-columns: 2fr 1fr" to "3fr 1fr" and observe how the article becomes wider.

Result: A magazine-style webpage is created using CSS Grid areas. It contains a header, navigation bar, main article, sidebar, and footer. The layout adjusts to smaller screens using a media query.

Submission:

- "index.html" — Magazine webpage
- "style.css" — Grid-area styling code
- Screenshot of the completed webpage