Assignment 6.5 — Profile Card Mini-Project

Objective

To create a responsive profile card using HTML and CSS while applying box model properties, backgrounds, borders, border-radius, positioning, and meaningful CSS class names.

Q1. What is a profile card?

Answer: A profile card is a component that displays information about a person, such as their profile image, name, role, description, skills, and contact details.

Q2. What is the CSS box model?

Answer: The CSS box model consists of four parts: content, padding, border, and margin. It determines how an element's size and spacing are calculated on a webpage.

Q3. Why do we use background, border, and border-radius?

Answer: Background properties add color or visual styling to an element. Borders create an outline around the element, while "border-radius" rounds its corners and improves its appearance.

Q4. What is the purpose of CSS positioning?

Answer: CSS positioning controls the placement of elements. In this project, "position: relative" is used on the card, and "position: absolute" is used to place a badge inside it.

Q5. Why are meaningful CSS class names important?

Answer: Meaningful class names make CSS easier to understand, maintain, and reuse. Examples include ".profile-card", ".profile-image", ".profile-skills", and ".contact-button".

Q6. Why should we test a card on different screen widths?

Answer: Testing different screen widths ensures that the card remains readable and properly arranged on mobile phones, tablets, and desktop screens. Responsive CSS helps prevent unwanted horizontal scrolling.

HTML Code

Create a file named "index.html" and paste the following code.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 6.5 - Profile Card</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <main class="page-container">
        <article class="profile-card">

            <span class="profile-badge">Student</span>

            <img
                class="profile-image"
                src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?w=300&h=300&fit=crop&crop=faces"
                alt="Profile portrait"
            >

            <h1 class="profile-name">Atul Yadav</h1>

            <h2 class="profile-role">B.Tech Student</h2>

            <p class="profile-description">
                I am a first-year B.Tech student interested in technology,
                web development, and learning new skills. I enjoy exploring
                creative ideas and working with others.
            </p>

            <div class="profile-skills">
                <span class="skill-tag">HTML</span>
                <span class="skill-tag">CSS</span>
                <span class="skill-tag">Communication</span>
                <span class="skill-tag">Teamwork</span>
            </div>

            <a class="contact-button" href="mailto:your-email@example.com">
                Contact Me
            </a>

        </article>
    </main>

</body>
</html>

CSS Code

Create a file named "style.css" in the same folder and paste this code.

* {
    box-sizing: border-box;
}

body {
    margin: 0;
    padding: 20px;
    font-family: Arial, sans-serif;
    color: #1e293b;
    background: linear-gradient(135deg, #dbeafe, #f5d0fe);
}

.page-container {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.profile-card {
    position: relative;
    width: 100%;
    max-width: 360px;
    padding: 30px 24px;
    margin: 20px auto;
    text-align: center;
    background-color: white;
    border: 1px solid #e2e8f0;
    border-radius: 20px;
    box-shadow: 0 10px 30px rgba(15, 23, 42, 0.12);
}

.profile-badge {
    position: absolute;
    top: 15px;
    right: 15px;
    padding: 6px 12px;
    color: white;
    background-color: #2563eb;
    border-radius: 20px;
    font-size: 12px;
    font-weight: bold;
}

.profile-image {
    display: block;
    width: 120px;
    height: 120px;
    max-width: 100%;
    margin: 15px auto 20px;
    border: 4px solid #bfdbfe;
    border-radius: 50%;
    object-fit: cover;
}

.profile-name {
    margin: 10px 0 5px;
    font-size: 26px;
    color: #0f172a;
}

.profile-role {
    margin: 0 0 15px;
    font-size: 16px;
    font-weight: normal;
    color: #2563eb;
}

.profile-description {
    margin: 0 0 20px;
    font-size: 14px;
    line-height: 1.7;
    color: #475569;
}

.profile-skills {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 25px;
}

.skill-tag {
    padding: 7px 10px;
    background-color: #eff6ff;
    border: 1px solid #bfdbfe;
    border-radius: 15px;
    font-size: 12px;
}

.contact-button {
    display: inline-block;
    width: 100%;
    padding: 12px 18px;
    color: white;
    background-color: #2563eb;
    border: 2px solid #2563eb;
    border-radius: 10px;
    text-decoration: none;
    font-weight: bold;
    transition: background-color 0.2s ease;
}

.contact-button:hover {
    background-color: #1d4ed8;
}

@media (max-width: 480px) {
    body {
        padding: 12px;
    }

    .profile-card {
        padding: 25px 18px;
    }

    .profile-name {
        font-size: 23px;
    }

    .profile-image {
        width: 105px;
        height: 105px;
    }
}

Result

The profile card displays a profile image, name, role, short description, skills, and a contact button. It uses CSS box model properties, a background gradient, borders, rounded corners, and absolute positioning for the badge. The responsive design adapts to smaller screens.

Conclusion

In this mini-project, I learned how to create a complete profile card using HTML and CSS. I applied padding, margin, borders, backgrounds, border-radius, positioning, and responsive design techniques to create a visually appealing component.

Submission Checklist

- [ ] "Assignment-6.5.md"
- [ ] "index.html"
- [ ] "style.css"
- [ ] Screenshot of the completed profile card
- [ ] Screenshot showing the card in mobile view