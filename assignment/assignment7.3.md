Assignment 7.3 — Responsive Product Listing

Objective

To create a responsive product listing webpage containing at least six product cards using HTML and CSS Flexbox. The project demonstrates "display: flex", "flex-wrap", "gap", "flex-grow", "flex-shrink", and "flex-basis".

Q1. What is a product listing?

Answer: A product listing is a webpage section that displays multiple products with their images, names, prices, and action buttons. It helps users view and compare different products.

Q2. What is "display: flex"?

Answer: The "display: flex" property creates a flex container. It allows child elements to be arranged in a row or column and provides control over their alignment and spacing.

Q3. What is the purpose of "flex-wrap: wrap"?

Answer: The "flex-wrap: wrap" property allows flex items to move onto the next line when there is not enough space on the current line. It helps create responsive product listings.

Q4. What does the "gap" property do?

Answer: The "gap" property creates space between flex items. It makes the layout cleaner and easier to maintain without adding margins to every card.

Q5. What is "flex-grow"?

Answer: The "flex-grow" property determines how much a flex item can grow to use available extra space. A value of "1" allows the item to grow when space is available.

Q6. What is "flex-shrink"?

Answer: The "flex-shrink" property determines how much a flex item can shrink when there is insufficient space. A value of "1" allows it to shrink, while "0" prevents it from shrinking due to the flex sizing algorithm.

Q7. What is "flex-basis"?

Answer: The "flex-basis" property defines the initial main size of a flex item before the remaining space is distributed. For example, "flex-basis: 240px" sets an initial width of 240 pixels in a row layout.

Q8. How does Flexbox make a product listing responsive?

Answer: Flexbox makes a product listing responsive by allowing cards to wrap onto new lines. Using "flex-wrap", "gap", a suitable "flex-basis", and responsive media queries helps the cards fit desktop, tablet, and mobile screens.

2. HTML Code

Create a file named "index.html" and paste the following code.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 7.3 - Responsive Product Listing</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="page-header">
        <h1>Tech Store</h1>
        <p>Discover useful products at great prices</p>
    </header>

    <main class="product-section">
        <h2 class="section-title">Our Products</h2>

        <div class="product-container">

            <article class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?w=500"
                    alt="Wireless headphones"
                    class="product-image"
                >
                <div class="product-details">
                    <h3>Wireless Headphones</h3>
                    <p class="product-price">₹1,499</p>
                    <p class="product-description">
                        Enjoy clear sound and comfortable listening.
                    </p>
                    <button class="product-button">View Product</button>
                </div>
            </article>

            <article class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?w=500"
                    alt="Classic wristwatch"
                    class="product-image"
                >
                <div class="product-details">
                    <h3>Classic Watch</h3>
                    <p class="product-price">₹2,199</p>
                    <p class="product-description">
                        A stylish watch for everyday use.
                    </p>
                    <button class="product-button">View Product</button>
                </div>
            </article>

            <article class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1503602642458-232111445657?w=500"
                    alt="Modern chair"
                    class="product-image"
                >
                <div class="product-details">
                    <h3>Modern Chair</h3>
                    <p class="product-price">₹3,499</p>
                    <p class="product-description">
                        A comfortable chair with a modern design.
                    </p>
                    <button class="product-button">View Product</button>
                </div>
            </article>

            <article class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?w=500"
                    alt="Red sports shoes"
                    class="product-image"
                >
                <div class="product-details">
                    <h3>Sports Shoes</h3>
                    <p class="product-price">₹1,899</p>
                    <p class="product-description">
                        Lightweight shoes for active days.
                    </p>
                    <button class="product-button">View Product</button>
                </div>
            </article>

            <article class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1511707171634-5f897ff02aa9?w=500"
                    alt="Smartphone"
                    class="product-image"
                >
                <div class="product-details">
                    <h3>Smartphone</h3>
                    <p class="product-price">₹12,999</p>
                    <p class="product-description">
                        A modern phone for everyday tasks.
                    </p>
                    <button class="product-button">View Product</button>
                </div>
            </article>

            <article class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?w=500"
                    alt="Studio headphones"
                    class="product-image"
                >
                <div class="product-details">
                    <h3>Studio Headphones</h3>
                    <p class="product-price">₹2,499</p>
                    <p class="product-description">
                        Comfortable headphones for music lovers.
                    </p>
                    <button class="product-button">View Product</button>
                </div>
            </article>

        </div>
    </main>

    <footer class="page-footer">
        <p>Assignment 7.3 | Responsive Product Listing</p>
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
    padding: 30px 20px;
    color: white;
    background-color: #0f172a;
    text-align: center;
}

.page-header h1 {
    margin-top: 0;
    font-size: 32px;
}

.product-section {
    max-width: 1200px;
    margin: 0 auto;
    padding: 35px 20px;
}

.section-title {
    margin: 0 0 25px;
    text-align: center;
    font-size: 28px;
}

/* Flexbox product layout */
.product-container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    align-items: stretch;
    gap: 24px;
}

/* flex-grow, flex-shrink, and flex-basis */
.product-card {
    display: flex;
    flex-direction: column;
    flex: 1 1 240px;
    max-width: 360px;
    min-width: 0;
    overflow: hidden;
    background-color: white;
    border: 1px solid #cbd5e1;
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(15, 23, 42, 0.08);
    transition: transform 0.2s ease;
}

.product-card:hover {
    transform: translateY(-4px);
}

.product-image {
    display: block;
    width: 100%;
    height: 200px;
    object-fit: cover;
    background-color: #e2e8f0;
}

.product-details {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    flex-grow: 1;
    padding: 18px;
}

.product-details h3 {
    margin: 0 0 10px;
    font-size: 19px;
}

.product-price {
    margin: 0 0 12px;
    color: #2563eb;
    font-size: 22px;
    font-weight: bold;
}

.product-description {
    margin: 0 0 20px;
    color: #64748b;
    font-size: 14px;
    line-height: 1.6;
}

.product-button {
    width: 100%;
    margin-top: auto;
    padding: 11px;
    color: white;
    background-color: #2563eb;
    border: none;
    border-radius: 7px;
    font-size: 14px;
    cursor: pointer;
}

.product-button:hover {
    background-color: #1d4ed8;
}

.page-footer {
    padding: 20px;
    color: white;
    background-color: #0f172a;
    text-align: center;
}

/* Mobile layout */
@media (max-width: 600px) {
    .product-section {
        padding: 25px 14px;
    }

    .product-container {
        gap: 16px;
    }

    .product-card {
        flex: 1 1 100%;
        max-width: 420px;
    }

    .product-image {
        height: 220px;
    }
}

4. Explanation of Important CSS Properties

Property| Purpose
"display: flex"| Arranges product cards using Flexbox.
"flex-wrap: wrap"| Moves cards to the next row when space is insufficient.
"gap: 24px"| Adds spacing between cards.
"flex-grow: 1"| Allows a card to grow when extra space is available.
"flex-shrink: 1"| Allows a card to shrink when necessary.
"flex-basis: 240px"| Sets the card's initial main size.
"justify-content: center"| Centers cards along the main axis.
"align-items: stretch"| Allows cards to stretch along the cross axis when appropriate.
"object-fit: cover"| Fills the image area without distorting the image.
"@media"| Adjusts the card layout for smaller screens.

In "flex: 1 1 240px", the three values represent "flex-grow", "flex-shrink", and "flex-basis", respectively.

5. Result

The responsive product listing was successfully created with six product cards. Each card contains an image, product name, price, description, and button. CSS Flexbox arranges the cards in rows on wider screens and allows them to wrap into a single-column layout on smaller screens.

6. Conclusion

In this assignment, I learned how to create a responsive product listing using HTML and CSS Flexbox. I practiced "flex-wrap", "gap", "flex-grow", "flex-shrink", and "flex-basis" to control the size, spacing, and arrangement of product cards on different screen widths.

7. Submission Checklist

- [ ] "Assignment-7.3.md"
- [ ] "index.html"
- [ ] "style.css"
- [ ] Desktop screenshot showing the product cards in multiple columns.
- [ ] Mobile screenshot showing the responsive card layout.