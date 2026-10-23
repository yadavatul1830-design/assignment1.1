Assignment 4.2 — Job Application Form

Q1. Create a job application form using different input types.

Answer: I created a job application form using HTML to collect personal details, qualifications, skills, and other information from applicants.

Q2. Add fields for full name, email, and phone.

Answer: I added input fields for full name, email address, and phone number using the appropriate HTML input types.

Q3. Add a date input for date of birth.

Answer: I used "<input type="date">" to allow applicants to select their date of birth.

Q4. Add a URL input for portfolio URL.

Answer: I used "<input type="url">" to allow applicants to enter their portfolio website address.

Q5. Add radio buttons for gender or preferred shift.

Answer: I added radio buttons for the preferred work shift. I used the same "name" attribute for related radio buttons so that only one option can be selected.

Q6. Add checkboxes for skills.

Answer: I used checkboxes to allow applicants to select multiple skills, such as communication, teamwork, and problem-solving.

Q7. Add a dropdown for qualification or job role and a textarea for the cover letter.

Answer: I used a "<select>" element to create a dropdown list for qualifications and a "<textarea>" element for applicants to write their cover letter.

Q8. Add labels, required fields, a disabled field, and a submit button.

Answer: I added labels for all fields, used the "required" attribute for mandatory information, included a disabled field as an example, and added a submit button to complete the form.

HTML Code — "job-application.html"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Job Application Form</title>
</head>
<body>

    <h1>Job Application Form</h1>

    <form action="#" method="post">

        <label for="fullName">Full Name:</label>
        <input type="text" id="fullName" name="fullName" required>
        <br><br>

        <label for="email">Email Address:</label>
        <input type="email" id="email" name="email" required>
        <br><br>

        <label for="phone">Phone Number:</label>
        <input type="tel" id="phone" name="phone" required>
        <br><br>

        <label for="dob">Date of Birth:</label>
        <input type="date" id="dob" name="dob" required>
        <br><br>

        <label for="portfolio">Portfolio URL:</label>
        <input type="url" id="portfolio" name="portfolio"
               placeholder="https://example.com">
        <br><br>

        <p>Preferred Shift:</p>

        <input type="radio" id="morning" name="shift"
               value="morning" required>
        <label for="morning">Morning</label>

        <input type="radio" id="evening" name="shift"
               value="evening">
        <label for="evening">Evening</label>
        <br><br>

        <p>Skills:</p>

        <input type="checkbox" id="communication"
               name="skills" value="communication">
        <label for="communication">Communication</label>
        <br>

        <input type="checkbox" id="teamwork"
               name="skills" value="teamwork">
        <label for="teamwork">Teamwork</label>
        <br>

        <input type="checkbox" id="problemSolving"
               name="skills" value="problem-solving">
        <label for="problemSolving">Problem Solving</label>
        <br><br>

        <label for="qualification">Highest Qualification:</label>
        <select id="qualification" name="qualification" required>
            <option value="">Select Qualification</option>
            <option value="diploma">Diploma</option>
            <option value="btech">B.Tech</option>
            <option value="bachelor">Other Bachelor's Degree</option>
            <option value="master">Master's Degree</option>
        </select>
        <br><br>

        <label for="coverLetter">Cover Letter:</label>
        <br>
        <textarea id="coverLetter" name="coverLetter"
                  rows="5" cols="40"
                  placeholder="Write your cover letter here..."></textarea>
        <br><br>

        <label for="applicationId">Application ID (Disabled):</label>
        <input type="text" id="applicationId" name="applicationId"
               value="Assigned by HR" disabled>
        <br><br>

        <button type="submit">Submit Application</button>

    </form>

</body>
</html>

Submission

1. "job-application.html" — Completed job application form.
2. Screenshot of the form opened in a web browser.

Note: Open the HTML file in a browser and check that the date picker, radio buttons, checkboxes, dropdown, cover letter area, and submit button work as expected. The form demonstrates HTML input controls; actual application submission requires a server-side handler.