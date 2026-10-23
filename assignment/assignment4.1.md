Assignment 4.1 — Student Registration Form

Q1. Build the form inside a "<form>" tag.

Answer: I created a student registration form using the HTML "<form>" tag to collect student details such as name, email, password, phone number, and age.

Q2. Add a proper "<label>" for each field.

Answer: I added a "<label>" for every input field to clearly identify the information required from the student.

Q3. Use correct input types, such as text, email, password, and number or a suitable tel.

Answer: I used appropriate input types: "text" for full name, "email" for email address, "password" for password, "tel" for phone number, and "number" for age.

Q4. Give each input a unique id and meaningful name.

Answer: I assigned a unique "id" and a meaningful "name" attribute to each input field so that the fields can be identified properly.

Q5. Add required on mandatory fields.

Answer: I used the "required" attribute on mandatory fields to ensure that students fill in the necessary information before submitting the form.

Q6. Complete the form with a submit button.

Answer: I added a submit button using "<button type="submit">" to allow students to submit their registration details.

HTML Code — "registration.html"

Save the following code in a file named "registration.html".

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Registration Form</title>
</head>
<body>

    <h1>Student Registration Form</h1>

    <form action="#" method="post">

        <label for="fullName">Full Name:</label>
        <input
            type="text"
            id="fullName"
            name="fullName"
            required
        >
        <br><br>

        <label for="email">Email:</label>
        <input
            type="email"
            id="email"
            name="email"
            required
        >
        <br><br>

        <label for="password">Password:</label>
        <input
            type="password"
            id="password"
            name="password"
            required
        >
        <br><br>

        <label for="phone">Phone Number:</label>
        <input
            type="tel"
            id="phone"
            name="phone"
            required
        >
        <br><br>

        <label for="age">Age:</label>
        <input
            type="number"
            id="age"
            name="age"
            min="1"
            max="120"
            required
        >
        <br><br>

        <button type="submit">Register</button>

    </form>

</body>
</html>

Submission

1. "registration.html" — Completed student registration form.
2. Screenshot showing the registration form opened in a web browser.

Note: Open "registration.html" in your browser and check that all fields and the Register button are displayed correctly.