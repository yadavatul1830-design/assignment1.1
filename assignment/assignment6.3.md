Assignment 6.3 — Overflow & Layout Fixing

1. Objective

To understand the CSS "overflow" property, create fixed-height containers, test different overflow values, and identify and fix a layout overflow issue.

2. Questions and Answers

Q1. What is the CSS overflow property?

Answer: The CSS "overflow" property controls what happens when content is larger than its container. It determines whether overflowing content is visible, hidden, or accessible through scrolling.

Q2. What is "overflow: visible"?

Answer: "overflow: visible" allows content to extend outside the container when it does not fit inside. It is the default overflow value.

Q3. What is "overflow: hidden"?

Answer: "overflow: hidden" clips content that extends beyond the container's boundaries. The hidden content cannot be accessed through scrolling.

Q4. What is "overflow: auto"?

Answer: "overflow: auto" automatically adds scrollbars when the content overflows the container. If scrolling is not needed, scrollbars are generally not shown.

Q5. What is "overflow: scroll"?

Answer: "overflow: scroll" makes the container scrollable and requests scrollbars even when the content fits inside it. The exact appearance of scrollbars depends on the browser and operating system.

Q6. What is the difference between "overflow: auto" and "overflow: scroll"?

Answer: "overflow: auto" displays scrollbars when necessary, while "overflow: scroll" requests scrollbars regardless of whether the content overflows.

Q7. What is a layout overflow issue?

Answer: A layout overflow issue occurs when content extends beyond its intended container or causes unwanted horizontal scrolling. It can be fixed by using suitable widths, "max-width", "box-sizing: border-box", and appropriate overflow settings.

Q8. How can we fix a layout overflow issue?

Answer: We can fix layout overflow by using responsive widths, setting "max-width: 100%", applying "box-sizing: border-box", and using "overflow: auto" when content needs to remain accessible through scrolling.

3. HTML Code

Create a file named "index.html" and paste the following code into it.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 6.3 - Overflow</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>CSS Overflow & Layout Fixing</h1>
        <p>Understanding different overflow values</p>
    </header>

    <main class="container">
        <section class="card">
            <h2>1. Overflow: Visible</h2>
            <div class="box visible">
                This is a long text used to demonstrate visible overflow.
                The content extends outside the fixed-height container.
                More text is added to make the overflow easy to observe.
                Extra content appears outside the box.
            </div>
        </section>

        <section class="card">
            <h2>2. Overflow: Hidden</h2>
            <div class="box hidden">
                This is a long text used to demonstrate hidden overflow.
                The content exceeds the fixed height of the container.
                The extra content is clipped and cannot be accessed
                using a scrollbar.
            </div>
        </section>

        <section class="card">
            <h2>3. Overflow: Auto</h2>
            <div class="box auto">
                This is a long text used to demonstrate automatic scrolling.
                When content exceeds the available height, a scrollbar
                appears so that the user can read the remaining content.
                Additional lines are included to demonstrate scrolling.
                Scroll down to read the complete text.
            </div>
        </section>

        <section class="card">
            <h2>4. Overflow: Scroll</h2>
            <div class="box scroll">
                This is a long text used to demonstrate scroll overflow.
                The container requests scrollbars even when they may
                not be necessary. Extra content allows us to test
                scrolling and observe the browser's behavior.
            </div>
        </section>

        <section class="card">
            <h2>5. Fixed Layout Example</h2>
            <div class="fixed-layout">
                <p>
                    This layout uses responsive width and box sizing
                    to prevent content from extending beyond its container.
                    The text wraps naturally on smaller screens.
                </p>
            </div>
        </section>
    </main>

    <footer>
        <p>Assignment 6.3 | CSS Overflow & Layout Fixing</p>
    </footer>

</body>
</html>

4. CSS Code

Create a file named "style.css" in the same folder and paste this code.

* {
    box-sizing: border-box;
}

body {
    margin: 0;
    padding: 20px;
    font-family: Arial, sans-serif;
    background-color: #f1f5f9;
    color: #1e293b;
}

header {
    text-align: center;
    background-color: #1d4ed8;
    color: white;
    padding: 20px;
    border-radius: 10px;
    margin-bottom: 25px;
}

.container {
    width: 100%;
    max-width: 900px;
    margin: 0 auto;
}

.card {
    background-color: white;
    padding: 20px;
    margin-bottom: 20px;
    border: 1px solid #cbd5e1;
    border-radius: 10px;
}

.card h2 {
    margin-top: 0;
    font-size: 20px;
}

.box {
    height: 100px;
    padding: 12px;
    border: 2px solid #2563eb;
    background-color: #dbeafe;
    line-height: 1.6;
}

.visible {
    overflow: visible;
    margin-bottom: 35px;
}

.hidden {
    overflow: hidden;
}

.auto {
    overflow: auto;
}

.scroll {
    overflow: scroll;
}

.fixed-layout {
    width: 100%;
    max-width: 100%;
    padding: 15px;
    border: 2px solid #16a34a;
    background-color: #dcfce7;
    overflow-wrap: anywhere;
}

.fixed-layout p {
    margin: 0;
    line-height: 1.6;
}

footer {
    text-align: center;
    margin-top: 25px;
    padding: 15px;
    background-color: #e2e8f0;
    border-radius: 8px;
}

@media (max-width: 600px) {
    body {
        padding: 10px;
    }

    .card {
        padding: 14px;
    }

    .card h2 {
        font-size: 18px;
    }
}

5. Practical Explanation

Overflow value| Behavior
"visible"| Extra content appears outside the box.
"hidden"| Extra content is clipped.
"auto"| Scrollbars appear when required.
"scroll"| Scrollbars are requested even when unnecessary.

The second container in the practical task uses "overflow: auto" so users can access content that exceeds its fixed height.

6. Layout Issue and Its Solution

Problem: A container may become wider than the screen because of excessive width, padding, borders, or long text.

Solution: The issue is addressed using:

- "box-sizing: border-box;" to include padding and borders in the element's declared width.
- "width: 100%;" to make the container fit its available space.
- "max-width: 900px;" to limit the main content width.
- "overflow-wrap: anywhere;" to allow long unbroken text to wrap when necessary.
- A media query to improve the layout on smaller screens.

7. Result

The webpage successfully demonstrates all four CSS overflow values: "visible", "hidden", "auto", and "scroll". A second scrollable container is implemented using "overflow: auto", and the sample layout is made responsive to prevent unwanted horizontal overflow.

8. Conclusion

In this assignment, I learned how the CSS overflow property manages content that exceeds a container's dimensions. I also learned how to fix common layout overflow issues using responsive widths, box sizing, text wrapping, and media queries.

9. Submission Checklist

- [ ] "Assignment-6.3.md"
- [ ] "index.html"
- [ ] "style.css"
- [ ] Screenshot showing all four overflow examples.
- [ ] Screenshot showing the corrected layout.