Assignment 6.2 — Backgrounds, Borders & Display

Objective

To create three differently styled cards using CSS backgrounds, borders, border-radius, and display properties.

Question 1: Create three cards named Basic, Standard, and Premium.

Answer:

I created three cards named Basic, Standard, and Premium using HTML "<div>" elements. Each card represents a different subscription plan and has a unique design.

Question 2: Add a title, description, and button to each card.

Answer:

Each card contains a title, a short description, and a button. These elements help users understand the features of each plan.

Question 3: Keep background colors and borders distinct.

Answer:

Different background colors and border styles are used for each card. The Basic card uses a light-blue background, the Standard card uses a light-green background, and the Premium card uses a light-purple background.

Question 4: Create rounded corners using "border-radius".

Answer:

The "border-radius" property is used to create rounded corners on the cards and buttons.

Example:

.card {
    border-radius: 15px;
}

Question 5: Demonstrate "display: block", "inline", and "inline-block" with practical examples.

Answer:

- "display: block": Elements start on a new line and generally occupy the available width.
- "display: inline": Elements remain on the same line and do not accept custom width and height in the usual way.
- "display: inline-block": Elements remain on the same line while allowing width and height to be set.

These properties are demonstrated using labels and sample boxes on the webpage.

Question 6: Set width, height, and "max-width".

Answer:

The "width" property sets an element's width, "height" sets its height, and "max-width" limits the maximum width an element can reach.

Example:

.card {
    width: 100%;
    max-width: 320px;
    min-height: 300px;
}

This helps keep the cards readable and responsive on different screen sizes.

Complete HTML File ("index.html")

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Backgrounds, Borders and Display</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>Choose Your Plan</h1>
        <p>Three different card designs using CSS.</p>
    </header>

    <main class="container">

        <section class="card basic">
            <h2>Basic</h2>
            <p class="price">Free</p>
            <p>Perfect for beginners who want to learn and explore.</p>
            <ul>
                <li>Basic features</li>
                <li>Community support</li>
                <li>Limited resources</li>
            </ul>
            <button type="button">Choose Basic</button>
        </section>

        <section class="card standard">
            <h2>Standard</h2>
            <p class="price">₹499/month</p>
            <p>Suitable for students who need more features.</p>
            <ul>
                <li>All basic features</li>
                <li>Priority support</li>
                <li>Extra resources</li>
            </ul>
            <button type="button">Choose Standard</button>
        </section>

        <section class="card premium">
            <h2>Premium</h2>
            <p class="price">₹999/month</p>
            <p>Designed for users who want the complete experience.</p>
            <ul>
                <li>All standard features</li>
                <li>Premium support</li>
                <li>Unlimited resources</li>
            </ul>
            <button type="button">Choose Premium</button>
        </section>

    </main>

    <section class="display-demo">
        <h2>CSS Display Properties</h2>

        <h3>1. Display: Block</h3>
        <div class="block-example">Block Element One</div>
        <div class="block-example">Block Element Two</div>

        <h3>2. Display: Inline</h3>
        <span class="inline-example">Inline One</span>
        <span class="inline-example">Inline Two</span>

        <h3>3. Display: Inline-Block</h3>
        <div class="inline-block-example">Inline-Block One</div>
        <div class="inline-block-example">Inline-Block Two</div>
    </section>

    <footer>
        <p>Assignment 6.2 — Backgrounds, Borders & Display</p>
    </footer>

</body>
</html>

Complete CSS File ("style.css")

/* General Styling */
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-color: #f4f6fa;
    color: #263238;
    line-height: 1.6;
}

header {
    text-align: center;
    padding: 30px 15px;
    background-color: #1e293b;
    color: white;
}

header h1 {
    margin-top: 0;
}

/* Cards Layout */
.container {
    display: flex;
    justify-content: center;
    align-items: stretch;
    flex-wrap: wrap;
    gap: 25px;
    max-width: 1100px;
    margin: 40px auto;
    padding: 20px;
}

/* Common Card Styling */
.card {
    width: 100%;
    max-width: 320px;
    min-height: 350px;
    padding: 25px;
    border-radius: 15px;
    text-align: center;
    display: flex;
    flex-direction: column;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
}

.card ul {
    text-align: left;
    padding-left: 25px;
}

.price {
    font-size: 24px;
    font-weight: bold;
}

/* Basic Card */
.basic {
    background-color: #e0f2fe;
    border: 3px solid #0284c7;
}

.basic h2 {
    color: #0369a1;
}

/* Standard Card */
.standard {
    background-color: #dcfce7;
    border: 3px solid #16a34a;
}

.standard h2 {
    color: #15803d;
}

/* Premium Card */
.premium {
    background-color: #f3e8ff;
    border: 3px solid #9333ea;
}

.premium h2 {
    color: #7e22ce;
}

/* Buttons */
.card button {
    margin-top: auto;
    padding: 12px 16px;
    border: none;
    border-radius: 8px;
    color: white;
    font-size: 15px;
    font-weight: bold;
    cursor: pointer;
}

.basic button {
    background-color: #0284c7;
}

.standard button {
    background-color: #16a34a;
}

.premium button {
    background-color: #9333ea;
}

/* Display Demonstrations */
.display-demo {
    max-width: 900px;
    margin: 30px auto;
    padding: 25px;
    background-color: white;
    border: 2px solid #cbd5e1;
    border-radius: 12px;
}

.block-example {
    display: block;
    width: 100%;
    max-width: 300px;
    padding: 10px;
    margin-bottom: 10px;
    background-color: #dbeafe;
    border: 1px solid #2563eb;
}

.inline-example {
    display: inline;
    background-color: #fef3c7;
    border: 1px solid #d97706;
    padding: 5px;
}

.inline-block-example {
    display: inline-block;
    width: 180px;
    height: 70px;
    padding: 15px;
    margin: 5px;
    background-color: #d1fae5;
    border: 1px solid #059669;
    text-align: center;
}

/* Footer */
footer {
    text-align: center;
    padding: 15px;
    margin-top: 30px;
    background-color: #1e293b;
    color: white;
}

/* Responsive Layout */
@media (max-width: 600px) {
    .container {
        flex-direction: column;
        align-items: center;
    }

    .display-demo {
        margin: 20px 12px;
    }
}

Result

The webpage was created successfully with three differently styled cards: Basic, Standard, and Premium. Different background colors, borders, rounded corners, widths, and heights were applied. The "block", "inline", and "inline-block" display properties were also demonstrated.

Conclusion

This assignment helped me understand how CSS backgrounds, borders, and display properties affect the appearance and layout of webpage elements. I also learned how to create attractive cards and use responsive widths for different screen sizes.

Submission

1. "index.html" — Contains the three cards and display-property examples.
2. "style.css" — Contains the styling for backgrounds, borders, cards, buttons, and display properties.
3. "Assignment-6.2.md" — Contains the questions, answers, result, and conclusion.