Assignment 8.2 — Auto-Responsive Image Gallery

Q1. What is an auto-responsive image gallery?

Answer: An auto-responsive image gallery is a webpage that displays multiple images in a grid. The number of columns automatically changes according to the screen size. CSS Grid makes it easy to create a responsive gallery for desktops, tablets, and mobile devices.

Q2. Collect at least eight images for the gallery.

Answer: We can use eight images of nature, mountains, beaches, flowers, and wildlife. These images will make the gallery attractive and help us test the responsive layout.

For this assignment, we will use sample images from Unsplash.

Q3. How do we place each image inside a gallery item?

Answer: Each image is placed inside a "<div>" with the class "gallery-item". This helps us style every image separately using CSS.

Example:

<div class="gallery-item">
    <img src="images/mountain.jpg" alt="Beautiful mountain">
</div>

The "src" attribute specifies the image location, and the "alt" attribute describes the image.

Q4. How does "grid-template-columns: repeat(auto-fit, minmax(...))" work?

Answer: This CSS property automatically adjusts the number of columns according to the available screen width.

Example:

.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
}

- "repeat()" repeats the column pattern.
- "auto-fit" fits as many columns as possible.
- "minmax(220px, 1fr)" keeps each column at least 220 pixels wide and allows it to grow.
- "gap: 20px" adds space between the images.

Q5. How do we make images fit properly inside the gallery?

Answer: We use "width: 100%" to make images fill their gallery items. The "object-fit: cover" property crops images when necessary so that they fit neatly without stretching.

Example:

.gallery-item img {
    width: 100%;
    height: 220px;
    object-fit: cover;
    display: block;
}

Q6. How do we maintain consistent spacing between gallery images?

Answer: The CSS "gap" property maintains equal spacing between rows and columns. We can also use padding, rounded corners, and shadows to improve the appearance of the gallery.

Example:

.gallery {
    display: grid;
    gap: 20px;
    padding: 20px;
}

.gallery-item {
    overflow: hidden;
    border-radius: 10px;
}

Q7. Create the complete responsive image gallery.

Answer: The following code creates a gallery containing eight images. Save the HTML and CSS in separate files.

File 1: "index.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="header">
        <h1>Nature Image Gallery</h1>
        <p>Explore the beauty of nature</p>
    </header>

    <main>
        <section class="gallery">
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?auto=format&fit=crop&w=800&q=80"
                     alt="Beautiful mountain landscape">
            </div>

            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?auto=format&fit=crop&w=800&q=80"
                     alt="Lake surrounded by mountains">
            </div>

            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?auto=format&fit=crop&w=800&q=80"
                     alt="Green forest and trees">
            </div>

            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=800&q=80"
                     alt="Scenic natural landscape">
            </div>

            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=800&q=80"
                     alt="Snow-covered mountain peaks">
            </div>

            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1470252649378-9c29740c9fa8?auto=format&fit=crop&w=800&q=80"
                     alt="Sunrise over a green landscape">
            </div>

            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=800&q=80"
                     alt="Blue sea and sandy beach">
            </div>

            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1511497584788-876760111969?auto=format&fit=crop&w=800&q=80"
                     alt="Sunlight passing through trees">
            </div>
        </section>
    </main>

    <footer class="footer">
        <p>Responsive Image Gallery using CSS Grid</p>
    </footer>

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

.header {
    text-align: center;
    background-color: #166534;
    color: white;
    padding: 30px 15px;
}

.header h1 {
    margin-bottom: 10px;
}

main {
    max-width: 1400px;
    margin: auto;
}

.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
    padding: 25px;
}

.gallery-item {
    overflow: hidden;
    border-radius: 10px;
    background-color: white;
    box-shadow: 0 3px 8px rgba(0, 0, 0, 0.12);
}

.gallery-item img {
    width: 100%;
    height: 220px;
    object-fit: cover;
    display: block;
    transition: transform 0.3s ease;
}

.gallery-item:hover img {
    transform: scale(1.05);
}

.footer {
    text-align: center;
    padding: 20px;
    background-color: #166534;
    color: white;
}

/* Smaller screens */
@media (max-width: 500px) {
    .gallery {
        grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
        gap: 12px;
        padding: 12px;
    }

    .gallery-item img {
        height: 170px;
    }

    .header h1 {
        font-size: 24px;
    }
}

Q8. How do we test the responsive gallery and submit the assignment?

Answer: Follow these steps:

1. Save the files as "index.html" and "style.css" in the same folder.
2. Open "index.html" in a web browser and check that all eight images load.
3. Right-click the page and select Inspect to open browser Developer Tools.
4. Resize the browser window or use the device toolbar to test different screen sizes.
5. Observe how the gallery automatically adjusts its columns on desktop and mobile screens.
6. Take one screenshot of the desktop layout and another of the mobile layout.

Result: An auto-responsive image gallery is created using CSS Grid. Eight images are displayed with consistent spacing, and the columns adjust automatically according to the available screen width.

Submission files:

- "index.html" — Gallery webpage
- "style.css" — Styling and responsive layout
- "desktop-screenshot.png" — Desktop view
- "mobile-screenshot.png" — Mobile view