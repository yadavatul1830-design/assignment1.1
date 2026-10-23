Assignment 6.1 — Box Model Inspection

Objective

To create a webpage with three boxes, apply different padding, borders, and margins, and understand the CSS box model using Chrome DevTools.

Question 1: Create three cards or boxes.

Answer:

I created three cards using HTML "<div>" elements. Each card contains a heading and a paragraph. CSS is used to style the cards differently.

Question 2: Add a heading and a paragraph to each box.

Answer:

Each box contains an "<h2>" heading and a "<p>" paragraph to demonstrate how content is displayed inside an HTML element.

Question 3: Apply different padding, border, and margin to each box.

Answer:

Padding is the space between content and the border. Border surrounds the padding and content. Margin is the space outside the border.

Different values are applied to each card to observe how these properties affect layout and spacing.

Question 4: Observe the difference between "box-sizing: content-box" and "box-sizing: border-box".

Answer:

- "content-box": The specified width applies only to the content. Padding and borders are added to the total width.
- "border-box": The specified width includes the content, padding, and border.

For example, if the width is 300px, padding is 20px on each side, and the border is 5px on each side:

- With "content-box", total width = 300 + 40 + 10 = 350px.
- With "border-box", total width = 300px.

Question 5: Inspect the box model diagram in Chrome DevTools.

Answer:

Steps:

1. Open "index.html" in Google Chrome.
2. Right-click on a card and select Inspect.
3. Open the Elements tab.
4. Select the card's HTML element.
5. Open the Computed panel.
6. Locate the box model diagram showing content, padding, border, and margin.
7. Change the padding, border, or margin values in the Styles panel and observe the changes.

Question 6: Take a screenshot and label the parts of the box model.

Answer:

I inspected a card using Chrome DevTools and captured a screenshot of the box model diagram. I labeled the four parts as follows:

1. Content: The area containing the heading and paragraph.
2. Padding: The space between the content and the border.
3. Border: The line surrounding the content and padding.
4. Margin: The outer space separating the card from other elements.

The screenshot demonstrates how each part affects the spacing and dimensions of an element.

Complete HTML File ("index.html")

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Box Model Inspection</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>CSS Box Model Inspection</h1>
        <p>Understanding content, padding, border, and margin.</p>
    </header>

    <main class="container">

        <div class="card card-one">
            <h2>Box One</h2>
            <p>This box uses content-box sizing with small padding,
            a solid border, and a moderate margin.</p>
        </div>

        <div class="card card-two">
            <h2>Box Two</h2>
            <p>This box uses border-box sizing with larger padding,
            a dashed border, and a different margin.</p>
        </div>

        <div class="card card-three">
            <h2>Box Three</h2>
            <p>This box uses border-box sizing with extra padding,
            a thicker border, and a larger margin.</p>
        </div>

        <section class="comparison">
            <h2>Box Sizing Comparison</h2>

            <div class="comparison-box content-example">
                <h3>Content-box</h3>
                <p>Width: 300px</p>
                <p>Padding: 20px</p>
                <p>Border: 5px</p>
                <p>Total width: 350px</p>
            </div>

            <div class="comparison-box border-example">
                <h3>Border-box</h3>
                <p>Width: 300px</p>
                <p>Padding: 20px</p>
                <p>Border: 5px</p>
                <p>Total width: 300px</p>
            </div>
        </section>

        <section class="box-parts">
            <h2>Four Parts of the CSS Box Model</h2>
            <div class="margin-layer">
                <span class="layer-label">MARGIN</span>
                <div class="border-layer">
                    <span class="layer-label">BORDER</span>
                    <div class="padding-layer">
                        <span class="layer-label">PADDING</span>
                        <div class="content-layer">
                            CONTENT
                        </div>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <footer>
        <p>Assignment 6.1 — Box Model Inspection</p>
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
    background-color: #f3f6fa;
    color: #263238;
    line-height: 1.6;
}

header {
    background-color: #1e3a8a;
    color: white;
    text-align: center;
    padding: 25px;
}

header h1 {
    margin-top: 0;
}

.container {
    max-width: 1000px;
    margin: 30px auto;
    padding: 20px;
}

/* Card One: Content-box */
.card-one {
    box-sizing: content-box;
    width: 300px;
    padding: 10px;
    border: 3px solid #2563eb;
    margin: 15px;
    background-color: white;
}

/* Card Two: Border-box */
.card-two {
    box-sizing: border-box;
    width: 350px;
    padding: 25px;
    border: 5px dashed #0d9488;
    margin: 30px 15px;
    background-color: #ecfdf5;
}

/* Card Three: Border-box */
.card-three {
    box-sizing: border-box;
    width: 400px;
    padding: 35px;
    border: 8px solid #ea580c;
    margin: 40px 15px;
    background-color: #fff7ed;
}

.card h2 {
    margin-top: 0;
}

/* Box Sizing Comparison */
.comparison {
    margin-top: 40px;
    padding: 20px;
    background-color: white;
}

.comparison-box {
    width: 300px;
    padding: 20px;
    border: 5px solid #1e3a8a;
    margin: 20px 0;
    background-color: #dbeafe;
}

.content-example {
    box-sizing: content-box;
}

.border-example {
    box-sizing: border-box;
}

/* Box Model Diagram */
.box-parts {
    margin-top: 40px;
    padding: 20px;
    background-color: white;
}

.margin-layer {
    background-color: #fef3c7;
    border: 2px dashed #b45309;
    padding: 25px;
    text-align: center;
}

.border-layer {
    background-color: #fca5a5;
    border: 8px solid #b91c1c;
    padding: 25px;
}

.padding-layer {
    background-color: #bbf7d0;
    padding: 25px;
}

.content-layer {
    background-color: #bfdbfe;
    border: 1px solid #1d4ed8;
    padding: 25px;
    font-weight: bold;
}

.layer-label {
    display: block;
    font-weight: bold;
    margin-bottom: 10px;
}

footer {
    background-color: #1e3a8a;
    color: white;
    text-align: center;
    padding: 15px;
    margin-top: 30px;
}

/* Responsive Design */
@media (max-width: 500px) {
    .container {
        padding: 10px;
    }

    .card-one,
    .card-two,
    .card-three,
    .comparison-box {
        width: 100%;
        margin: 15px 0;
    }
}

Result

The webpage was created successfully with three cards using different padding, borders, and margins. The difference between "content-box" and "border-box" was demonstrated. The four parts of the CSS box model were also illustrated.

Conclusion

This assignment helped me understand the CSS box model and how content, padding, border, and margin affect element dimensions and spacing. I also learned to inspect and modify box model properties using Chrome DevTools.

Submission

1. "index.html" — HTML webpage containing three cards and a box model diagram.
2. "style.css" — CSS stylesheet containing box model properties.
3. "box-model-screenshot.png" — Annotated screenshot of the box model in Chrome DevTools.