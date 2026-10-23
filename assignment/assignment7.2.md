Assignment 7.2 — Pricing Cards & Centered Login Form

Objective

To create three aligned pricing cards named Basic, Pro, and Premium using CSS Flexbox, and to design a login form centered horizontally and vertically. The project demonstrates "flex-direction", "justify-content", "align-items", and responsive design.

Q1. What are pricing cards?

Answer: Pricing cards are website components that display the price, features, and action button for different products or subscription plans. They help users compare available plans.

Q2. What is CSS Flexbox?

Answer: CSS Flexbox is a layout model that arranges elements in rows or columns and helps distribute space and align items inside a container.

Q3. What is the purpose of "justify-content"?

Answer: The "justify-content" property aligns and distributes flex items along the main axis. For example, "justify-content: center" centers items, while "justify-content: space-between" distributes space between them.

Q4. What is the purpose of "align-items"?

Answer: The "align-items" property aligns flex items along the cross axis. It can be used to align cards vertically or center a form inside a container.

Q5. What does "flex-direction" do?

Answer: The "flex-direction" property determines the direction in which flex items are arranged. The values "row" and "column" arrange items horizontally and vertically, respectively.

Q6. How can we center a login form horizontally and vertically?

Answer: We can use a flex container with "display: flex", "justify-content: center", and "align-items: center". A suitable "min-height" ensures that the container has enough height to center the form vertically.

Q7. Why is responsive design important?

Answer: Responsive design allows a webpage to adjust to different screen sizes. Media queries can stack pricing cards vertically on smaller screens and keep them aligned horizontally on larger screens.

Q8. What is the purpose of a pricing button?

Answer: A pricing button allows users to select a plan or proceed to the next step. In this practice project, the buttons demonstrate the design of plan selection actions.

2. HTML Code

Create a file named "index.html" and paste the following code.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 7.2 - Pricing Cards and Login Form</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="page-header">
        <h1>Choose Your Plan</h1>
        <p>Simple plans for different needs</p>
    </header>

    <main>
        <section class="pricing-section">
            <div class="pricing-container">

                <article class="pricing-card">
                    <h2>Basic</h2>
                    <p class="price">₹199<span>/month</span></p>
                    <ul class="features">
                        <li>5 Projects</li>
                        <li>Basic Support</li>
                        <li>10 GB Storage</li>
                    </ul>
                    <button class="plan-button">Choose Basic</button>
                </article>

                <article class="pricing-card featured">
                    <span class="popular-badge">Popular</span>
                    <h2>Pro</h2>
                    <p class="price">₹499<span>/month</span></p>
                    <ul class="features">
                        <li>20 Projects</li>
                        <li>Priority Support</li>
                        <li>50 GB Storage</li>
                    </ul>
                    <button class="plan-button">Choose Pro</button>
                </article>

                <article class="pricing-card">
                    <h2>Premium</h2>
                    <p class="price">₹999<span>/month</span></p>
                    <ul class="features">
                        <li>Unlimited Projects</li>
                        <li>Premium Support</li>
                        <li>200 GB Storage</li>
                    </ul>
                    <button class="plan-button">Choose Premium</button>
                </article>

            </div>
        </section>

        <section class="login-section">
            <form class="login-form">
                <h2>Login</h2>
                <p>Welcome back! Enter your details.</p>

                <label for="email">Email Address</label>
                <input
                    type="email"
                    id="email"
                    name="email"
                    placeholder="Enter your email"
                    required
                >

                <label for="password">Password</label>
                <input
                    type="password"
                    id="password"
                    name="password"
                    placeholder="Enter your password"
                    required
                >

                <button type="submit" class="login-button">Login</button>
            </form>
        </section>
    </main>

    <footer class="page-footer">
        <p>Assignment 7.2 | Flexbox Layout Practice</p>
    </footer>

</body>
</html>

3. CSS Code

Create a file named "style.css" in the same folder and paste this code.

* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    color: #1e293b;
    background-color: #f1f5f9;
}

.page-header {
    padding: 30px 15px;
    text-align: center;
    color: white;
    background-color: #1e3a8a;
}

.page-header h1 {
    margin-top: 0;
}

.pricing-section {
    padding: 40px 20px;
}

.pricing-container {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: stretch;
    flex-wrap: wrap;
    gap: 25px;
    max-width: 1100px;
    margin: 0 auto;
}

.pricing-card {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    flex: 1 1 260px;
    max-width: 320px;
    padding: 30px 22px;
    background-color: white;
    border: 1px solid #cbd5e1;
    border-radius: 14px;
    box-shadow: 0 5px 15px rgba(15, 23, 42, 0.08);
    text-align: center;
}

.pricing-card h2 {
    margin: 0 0 15px;
    font-size: 25px;
}

.featured {
    border: 2px solid #2563eb;
}

.popular-badge {
    position: absolute;
    top: -13px;
    padding: 5px 14px;
    color: white;
    background-color: #2563eb;
    border-radius: 20px;
    font-size: 12px;
    font-weight: bold;
}

.price {
    margin: 10px 0 20px;
    font-size: 30px;
    font-weight: bold;
    color: #1d4ed8;
}

.price span {
    font-size: 13px;
    font-weight: normal;
    color: #64748b;
}

.features {
    align-self: stretch;
    margin: 0 0 25px;
    padding-left: 25px;
    text-align: left;
    line-height: 2.2;
}

.plan-button {
    width: 100%;
    margin-top: auto;
    padding: 12px;
    color: white;
    background-color: #2563eb;
    border: none;
    border-radius: 7px;
    font-size: 15px;
    cursor: pointer;
}

.plan-button:hover {
    background-color: #1d4ed8;
}

.login-section {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    padding: 30px 15px;
    background: linear-gradient(135deg, #dbeafe, #ede9fe);
}

.login-form {
    display: flex;
    flex-direction: column;
    gap: 12px;
    width: 100%;
    max-width: 380px;
    padding: 30px;
    background-color: white;
    border: 1px solid #e2e8f0;
    border-radius: 14px;
    box-shadow: 0 8px 25px rgba(15, 23, 42, 0.1);
}

.login-form h2 {
    margin: 0;
    text-align: center;
}

.login-form p {
    margin: 0 0 10px;
    color: #64748b;
    text-align: center;
}

.login-form label {
    font-size: 14px;
    font-weight: bold;
}

.login-form input {
    width: 100%;
    padding: 12px;
    border: 1px solid #cbd5e1;
    border-radius: 7px;
    font-size: 14px;
}

.login-form input:focus {
    outline: 2px solid #93c5fd;
    border-color: #2563eb;
}

.login-button {
    margin-top: 8px;
    padding: 12px;
    color: white;
    background-color: #1e3a8a;
    border: none;
    border-radius: 7px;
    font-size: 15px;
    cursor: pointer;
}

.page-footer {
    padding: 20px;
    color: white;
    background-color: #0f172a;
    text-align: center;
}

@media (max-width: 600px) {
    .pricing-container {
        flex-direction: column;
        align-items: center;
    }

    .pricing-card {
        width: 100%;
        max-width: 380px;
        flex: none;
    }

    .pricing-section {
        padding: 30px 15px;
    }

    .login-form {
        padding: 24px 18px;
    }
}

4. Explanation of Important CSS Properties

Property| Purpose
"display: flex"| Creates a Flexbox layout.
"flex-direction: row"| Places pricing cards horizontally.
"flex-direction: column"| Stacks the login form fields vertically and pricing cards on mobile.
"justify-content: center"| Centers items along the main axis.
"align-items: center"| Aligns items along the cross axis.
"align-items: stretch"| Makes cards stretch to a shared height when the flex layout allows it.
"flex-wrap: wrap"| Allows cards to wrap onto another line when necessary.
"gap"| Adds space between cards or form fields.
"min-height: 100vh"| Gives the login section at least the height of the viewport.
"max-width"| Prevents cards and the login form from becoming excessively wide.

5. Result

The webpage displays three pricing cards named Basic, Pro, and Premium, each with a price, feature list, and button. The cards are arranged using Flexbox and adapt to smaller screens. The login form is centered horizontally and vertically within its section, and its fields are arranged vertically using "flex-direction: column".

6. Conclusion

In this assignment, I learned how to build pricing cards and a centered login form using HTML and CSS Flexbox. I practiced "flex-direction", "justify-content", "align-items", "flex-wrap", and "gap", and learned how media queries help create responsive layouts.

7. Submission Checklist

- [ ] "Assignment-7.2.md"
- [ ] "index.html"
- [ ] "style.css"
- [ ] Screenshot showing all three pricing cards.
- [ ] Screenshot showing the centered login form.
- [ ] Screenshot showing the responsive layout on a smaller screen.