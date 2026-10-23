Assignment 8.4 — Dashboard with Grid and Flexbox

1. Objective

The objective of this assignment is to create a responsive dashboard using CSS Grid and Flexbox. CSS Grid is used to organize the overall dashboard layout, while Flexbox is used to align icons, titles, and numbers inside statistic cards. The dashboard also includes a header, sidebar, four statistic cards, and a recent activity table.

2. Questions and Answers

Q1. What is a dashboard?

Answer: A dashboard is a user interface that displays important information, statistics, and activities in an organized format.

Q2. What is CSS Grid?

Answer: CSS Grid is a two-dimensional CSS layout system that arranges elements into rows and columns. It is useful for creating complex page layouts.

Q3. What is Flexbox?

Answer: Flexbox is a one-dimensional CSS layout system that arranges elements in a row or column and helps align and distribute space between them.

Q4. What is the difference between Grid and Flexbox?

Answer: CSS Grid is mainly used to manage layouts across rows and columns, whereas Flexbox is mainly used to align and distribute items along one direction.

Q5. Why is CSS Grid used for the dashboard layout?

Answer: CSS Grid is used to divide the dashboard into major areas, such as the header, sidebar, and main content area.

Q6. Why is Flexbox used inside statistic cards?

Answer: Flexbox helps align the card title, icon, and statistic number neatly and maintains consistent spacing between the elements.

Q7. What is the purpose of "grid-template-areas"?

Answer: The "grid-template-areas" property assigns names to specific areas of a CSS Grid layout, making the page structure easier to understand and manage.

Q8. What is the purpose of "gap" in CSS?

Answer: The "gap" property adds consistent spacing between Grid tracks or Flexbox items without requiring individual margins.

Q9. What is a media query?

Answer: A media query applies CSS rules based on conditions such as screen width. It helps make a website responsive on desktops, tablets, and mobile devices.

Q10. What is the Grid Inspector in browser DevTools?

Answer: The Grid Inspector is a browser developer tool that visually displays CSS Grid rows, columns, and layout areas. It helps developers inspect and debug Grid layouts.

3. Project Structure

Create the following files in the same folder:

Assignment-8.4/
├── index.html
└── style.css

4. HTML Code ("index.html")

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DashFlow - Admin Dashboard</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="dashboard">

        <!-- Header -->
        <header class="header">
            <a href="#" class="brand">DashFlow</a>

            <div class="header-right">
                <span class="welcome">Welcome, Atul!</span>
                <div class="avatar">AY</div>
            </div>
        </header>

        <!-- Sidebar -->
        <aside class="sidebar">
            <p class="sidebar-label">MAIN MENU</p>

            <nav class="sidebar-nav">
                <a href="#" class="nav-item active">
                    <span class="nav-icon">▦</span>
                    Dashboard
                </a>

                <a href="#statistics" class="nav-item">
                    <span class="nav-icon">▤</span>
                    Analytics
                </a>

                <a href="#activity" class="nav-item">
                    <span class="nav-icon">◷</span>
                    Activity
                </a>

                <a href="#reports" class="nav-item">
                    <span class="nav-icon">▧</span>
                    Reports
                </a>

                <a href="#settings" class="nav-item">
                    <span class="nav-icon">⚙</span>
                    Settings
                </a>
            </nav>

            <div class="sidebar-bottom">
                <p>DashFlow Dashboard</p>
                <small>Simple insights. Better decisions.</small>
            </div>
        </aside>

        <!-- Main Content -->
        <main class="main-content">

            <section class="page-heading">
                <div>
                    <p class="eyebrow">OVERVIEW</p>
                    <h1>Dashboard</h1>
                    <p class="subtitle">
                        Here is what's happening with your business today.
                    </p>
                </div>

                <span class="date-badge">● Live Overview</span>
            </section>

            <!-- Statistics Cards -->
            <section class="stats-grid" id="statistics">

                <article class="stat-card">
                    <div class="stat-top">
                        <span class="stat-title">Total Revenue</span>
                        <span class="stat-icon purple">₹</span>
                    </div>
                    <div class="stat-bottom">
                        <h2>₹84,250</h2>
                        <span class="trend positive">+12.5%</span>
                    </div>
                    <p class="stat-note">Compared with last month</p>
                </article>

                <article class="stat-card">
                    <div class="stat-top">
                        <span class="stat-title">Total Users</span>
                        <span class="stat-icon blue">♙</span>
                    </div>
                    <div class="stat-bottom">
                        <h2>2,450</h2>
                        <span class="trend positive">+8.2%</span>
                    </div>
                    <p class="stat-note">Compared with last month</p>
                </article>

                <article class="stat-card">
                    <div class="stat-top">
                        <span class="stat-title">Orders</span>
                        <span class="stat-icon orange">▣</span>
                    </div>
                    <div class="stat-bottom">
                        <h2>1,280</h2>
                        <span class="trend positive">+5.7%</span>
                    </div>
                    <p class="stat-note">Compared with last month</p>
                </article>

                <article class="stat-card">
                    <div class="stat-top">
                        <span class="stat-title">Pending Tasks</span>
                        <span class="stat-icon green">✓</span>
                    </div>
                    <div class="stat-bottom">
                        <h2>18</h2>
                        <span class="trend neutral">In progress</span>
                    </div>
                    <p class="stat-note">Tasks requiring attention</p>
                </article>

            </section>

            <!-- Recent Activity Table -->
            <section class="activity-section" id="activity">
                <div class="section-heading">
                    <div>
                        <h2>Recent Activity</h2>
                        <p>Latest updates from your dashboard</p>
                    </div>

                    <span class="table-badge">Sample Data</span>
                </div>

                <div class="table-wrapper">
                    <table>
                        <thead>
                            <tr>
                                <th>Activity</th>
                                <th>Date</th>
                                <th>Status</th>
                            </tr>
                        </thead>

                        <tbody>
                            <tr>
                                <td>
                                    <strong>New user registered</strong>
                                    <small>Account creation</small>
                                </td>
                                <td>23 Oct 2026</td>
                                <td>
                                    <span class="status completed">
                                        Completed
                                    </span>
                                </td>
                            </tr>

                            <tr>
                                <td>
                                    <strong>Order received</strong>
                                    <small>Order #DF1024</small>
                                </td>
                                <td>22 Oct 2026</td>
                                <td>
                                    <span class="status pending">
                                        Pending
                                    </span>
                                </td>
                            </tr>

                            <tr>
                                <td>
                                    <strong>Monthly report</strong>
                                    <small>Analytics report</small>
                                </td>
                                <td>21 Oct 2026</td>
                                <td>
                                    <span class="status completed">
                                        Completed
                                    </span>
                                </td>
                            </tr>

                            <tr>
                                <td>
                                    <strong>Payment review</strong>
                                    <small>Transaction #TX204</small>
                                </td>
                                <td>20 Oct 2026</td>
                                <td>
                                    <span class="status review">
                                        In Review
                                    </span>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </section>

            <footer class="main-footer" id="reports">
                Dashboard project built using HTML, CSS Grid, and Flexbox.
            </footer>

        </main>

    </div>

</body>
</html>

5. CSS Code ("style.css")

/* Global Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background: #f4f6fb;
    color: #1e293b;
    line-height: 1.5;
    overflow-wrap: break-word;
}

a {
    text-decoration: none;
    color: inherit;
}

/* Outer Dashboard Grid */
.dashboard {
    min-height: 100vh;
    display: grid;

    grid-template-columns: 245px minmax(0, 1fr);
    grid-template-rows: 72px minmax(0, 1fr);

    grid-template-areas:
        "header header"
        "sidebar main";
}

/* Header */
.header {
    grid-area: header;
    background: #ffffff;
    border-bottom: 1px solid #e8ecf3;
    padding: 0 30px;

    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
}

.brand {
    color: #4f46e5;
    font-size: 1.65rem;
    font-weight: 800;
    letter-spacing: -1px;
}

.header-right {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    gap: 14px;
    flex-wrap: wrap;
}

.welcome {
    color: #475569;
    font-size: 0.95rem;
    font-weight: 600;
}

.avatar {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background: #e0e7ff;
    color: #4338ca;

    display: flex;
    justify-content: center;
    align-items: center;

    font-weight: 800;
}

/* Sidebar */
.sidebar {
    grid-area: sidebar;
    background: #ffffff;
    border-right: 1px solid #e8ecf3;
    padding: 28px 16px;

    display: flex;
    flex-direction: column;
    gap: 24px;
}

.sidebar-label {
    padding: 0 12px;
    color: #94a3b8;
    font-size: 0.72rem;
    font-weight: 800;
    letter-spacing: 1.5px;
}

.sidebar-nav {
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.nav-item {
    display: flex;
    align-items: center;
    gap: 12px;

    padding: 12px;
    border-radius: 9px;
    color: #64748b;
    font-size: 0.94rem;
    font-weight: 600;

    transition: background-color 0.2s ease,
                color 0.2s ease;
}

.nav-item:hover,
.nav-item.active {
    background: #eef2ff;
    color: #4f46e5;
}

.nav-icon {
    width: 24px;
    text-align: center;
    font-size: 1.15rem;
}

.sidebar-bottom {
    margin-top: auto;
    padding: 16px 12px;
    border-top: 1px solid #e8ecf3;
    color: #475569;
    font-size: 0.88rem;
}

.sidebar-bottom small {
    display: block;
    margin-top: 5px;
    color: #94a3b8;
}

/* Main Content */
.main-content {
    grid-area: main;
    min-width: 0;
    padding: 32px;
}

.page-heading {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
    flex-wrap: wrap;
    margin-bottom: 28px;
}

.eyebrow {
    color: #4f46e5;
    font-size: 0.75rem;
    font-weight: 800;
    letter-spacing: 1.5px;
    margin-bottom: 6px;
}

.page-heading h1 {
    font-size: clamp(1.8rem, 3vw, 2.2rem);
    line-height: 1.2;
    margin-bottom: 8px;
}

.subtitle {
    color: #64748b;
    font-size: 0.95rem;
}

.date-badge {
    background: #ffffff;
    border: 1px solid #e2e8f0;
    border-radius: 20px;
    padding: 9px 14px;
    color: #475569;
    font-size: 0.82rem;
    white-space: nowrap;
}

/* Four Statistic Cards */
.stats-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 20px;
    margin-bottom: 30px;
}

.stat-card {
    min-width: 0;
    padding: 22px;
    background: #ffffff;
    border: 1px solid #e8ecf3;
    border-radius: 14px;
    box-shadow: 0 4px 14px rgba(15, 23, 42, 0.03);
}

/* Inner Flexbox Layout */
.stat-top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 12px;
    margin-bottom: 20px;
}

.stat-title {
    color: #64748b;
    font-size: 0.88rem;
    font-weight: 600;
}

.stat-icon {
    width: 42px;
    height: 42px;
    flex-shrink: 0;
    border-radius: 11px;

    display: flex;
    justify-content: center;
    align-items: center;

    font-size: 1.3rem;
    font-weight: 800;
}

.purple {
    background: #ede9fe;
    color: #7c3aed;
}

.blue {
    background: #dbeafe;
    color: #2563eb;
}

.orange {
    background: #ffedd5;
    color: #ea580c;
}

.green {
    background: #dcfce7;
    color: #16a34a;
}

.stat-bottom {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 10px;
    flex-wrap: wrap;
    margin-bottom: 8px;
}

.stat-bottom h2 {
    font-size: clamp(1.25rem, 2vw, 1.8rem);
    letter-spacing: -0.5px;
    overflow-wrap: anywhere;
}

.trend {
    font-size: 0.75rem;
    font-weight: 800;
}

.positive {
    color: #16a34a;
}

.neutral {
    color: #d97706;
}

.stat-note {
    color: #94a3b8;
    font-size: 0.78rem;
}

/* Recent Activity Table */
.activity-section {
    background: #ffffff;
    border: 1px solid #e8ecf3;
    border-radius: 14px;
    padding: 24px;
    min-width: 0;
}

.section-heading {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 16px;
    flex-wrap: wrap;
    margin-bottom: 22px;
}

.section-heading h2 {
    font-size: 1.2rem;
    margin-bottom: 5px;
}

.section-heading p {
    color: #94a3b8;
    font-size: 0.86rem;
}

.table-badge {
    background: #f1f5f9;
    color: #64748b;
    border-radius: 6px;
    padding: 6px 10px;
    font-size: 0.75rem;
    font-weight: 700;
}

.table-wrapper {
    width: 100%;
    overflow-x: auto;
}

table {
    width: 100%;
    min-width: 480px;
    border-collapse: collapse;
    text-align: left;
}

th {
    background: #f8fafc;
    color: #64748b;
    font-size: 0.78rem;
    font-weight: 700;
}

th,
td {
    padding: 15px 12px;
    border-bottom: 1px solid #edf0f5;
}

tbody tr:last-child td {
    border-bottom: none;
}

td {
    color: #475569;
    font-size: 0.85rem;
}

td strong {
    display: block;
    color: #1e293b;
    font-size: 0.86rem;
}

td small {
    display: block;
    color: #94a3b8;
    margin-top: 4px;
}

.status {
    display: inline-block;
    padding: 5px 9px;
    border-radius: 20px;
    font-size: 0.74rem;
    font-weight: 700;
    white-space: nowrap;
}

.completed {
    background: #dcfce7;
    color: #15803d;
}

.pending {
    background: #fef3c7;
    color: #b45309;
}

.review {
    background: #dbeafe;
    color: #1d4ed8;
}

/* Footer */
.main-footer {
    padding: 24px 0 8px;
    text-align: center;
    color: #94a3b8;
    font-size: 0.8rem;
}

/* Tablet Responsive Layout */
@media (max-width: 1100px) {
    .stats-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .main-content {
        padding: 24px;
    }
}

/* Mobile Responsive Layout */
@media (max-width: 700px) {
    .dashboard {
        grid-template-columns: minmax(0, 1fr);
        grid-template-rows: auto auto minmax(0, 1fr);

        grid-template-areas:
            "header"
            "sidebar"
            "main";
    }

    .header {
        min-height: 70px;
        padding: 14px 18px;
    }

    .welcome {
        display: none;
    }

    .sidebar {
        padding: 12px 16px;
        gap: 12px;
        border-right: none;
        border-bottom: 1px solid #e8ecf3;
    }

    .sidebar-label,
    .sidebar-bottom {
        display: none;
    }

    .sidebar-nav {
        flex-direction: row;
        flex-wrap: wrap;
        gap: 8px;
    }

    .nav-item {
        flex: 1 1 auto;
        justify-content: center;
        padding: 10px;
        font-size: 0.82rem;
    }

    .main-content {
        padding: 22px 16px;
    }

    .stats-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 12px;
    }

    .stat-card {
        padding: 16px;
    }

    .activity-section {
        padding: 16px;
    }
}

/* Small Mobile Screens */
@media (max-width: 400px) {
    .stats-grid {
        grid-template-columns: minmax(0, 1fr);
    }

    .header {
        padding: 12px;
    }

    .brand {
        font-size: 1.4rem;
    }

    .main-content {
        padding: 18px 12px;
    }

    .page-heading {
        align-items: flex-start;
    }

    .nav-item {
        flex-basis: 100%;
        justify-content: flex-start;
    }
}

6. Explanation of Important CSS Properties

Property| Purpose
"display: grid"| Creates a Grid layout for the dashboard.
"grid-template-columns"| Defines the width and number of columns.
"grid-template-areas"| Assigns named areas to the header, sidebar, and main content.
"display: flex"| Aligns elements inside the header, sidebar, and statistic cards.
"justify-content"| Controls item distribution along the main axis.
"align-items"| Aligns items along the cross axis.
"gap"| Adds consistent spacing between items.
"minmax(0, 1fr)"| Allows a Grid track to shrink without exceeding available space.
"flex-wrap: wrap"| Allows Flexbox items to move to another line when necessary.
"overflow-x: auto"| Allows horizontal scrolling for the activity table on narrow screens.
"@media"| Changes the layout for tablets and mobile screens.

7. Grid and Flexbox Implementation

CSS Grid is used for:

- The outer dashboard layout.
- Separating the header, sidebar, and main content.
- Arranging the four statistic cards into responsive columns.

Flexbox is used for:

- Aligning the logo and profile section in the header.
- Arranging the sidebar links.
- Aligning icons, titles, and numbers inside statistic cards.
- Distributing the page heading and activity section labels.

8. Result

The completed dashboard displays a header, sidebar, four statistic cards, and a recent activity table. The outer layout is created with CSS Grid, while Flexbox is used for internal alignment and spacing. Media queries adapt the layout to tablet and mobile screens.

The dashboard uses a consistent color palette, readable typography, and spacing to provide a clean interface.

9. Conclusion

This assignment demonstrates the combined use of CSS Grid and Flexbox to create a responsive dashboard. Grid organizes the main page structure, while Flexbox aligns the elements inside individual components. Responsive media queries and overflow handling help maintain usability across different screen sizes.

10. Submission Checklist

- [ ] Create "index.html".
- [ ] Create "style.css".
- [ ] Keep both files in the same folder.
- [ ] Open the HTML file in a browser and verify the dashboard.
- [ ] Test the layout at desktop, tablet, and mobile widths.
- [ ] Inspect the outer Grid using browser DevTools.
- [ ] Take screenshots of the completed dashboard.
- [ ] Submit both HTML and CSS files.