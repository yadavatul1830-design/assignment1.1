Assignment 4.3 — Student Marks Table

Q1. What is the purpose of a student marksheet table?

Answer: A student marksheet table displays students' names, marks in different subjects, and their total marks in an organized format.

Q2. Add data for at least 5 students and 3 subjects.

Answer: The table includes five students and three subjects: HTML, CSS, and JavaScript.

Q3. Use "<table>", "<tr>", "<th>", and "<td>" tags.

Answer:

- "<table>" creates the table.
- "<tr>" creates a row.
- "<th>" creates a header cell.
- "<td>" creates a data cell.

Q4. Organize the table using "<thead>", "<tbody>", and "<tfoot>".

Answer:

- "<thead>" contains the table headings.
- "<tbody>" contains student marks.
- "<tfoot>" displays the total or average marks.

Q5. Give a title to the table using "<caption>".

Answer: The "<caption>" tag adds the title Student Marksheet above the table.

Q6. Show total or average marks in the footer.

Answer: The footer displays the total marks obtained by all five students and the average marks per student.

Q7. Use "colspan" or "rowspan" where appropriate.

Answer: The "colspan" attribute combines multiple columns into one cell. In this table, it is used to display the footer heading across several columns.

Q8. Why should table headers be meaningful?

Answer: Meaningful headers help users understand the information in each column, such as student name, subject marks, and total marks.

---

HTML Code: "marksheet.html"

Save the following code in a file named "marksheet.html".

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Marksheet</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 30px;
            background-color: #f4f6f8;
        }

        h1 {
            text-align: center;
            color: #243b55;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            background-color: white;
        }

        caption {
            font-size: 22px;
            font-weight: bold;
            padding: 12px;
        }

        th, td {
            border: 1px solid #333;
            padding: 12px;
            text-align: center;
        }

        thead {
            background-color: #dbeafe;
        }

        tfoot {
            background-color: #e2e8f0;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <h1>Student Marks Report</h1>

    <table>
        <caption>Student Marksheet</caption>

        <thead>
            <tr>
                <th scope="col">Roll No.</th>
                <th scope="col">Student Name</th>
                <th scope="col">HTML</th>
                <th scope="col">CSS</th>
                <th scope="col">JavaScript</th>
                <th scope="col">Total Marks</th>
            </tr>
        </thead>

        <tbody>
            <tr>
                <td>101</td>
                <td>Rahul</td>
                <td>85</td>
                <td>78</td>
                <td>90</td>
                <td>253</td>
            </tr>
            <tr>
                <td>102</td>
                <td>Priya</td>
                <td>92</td>
                <td>88</td>
                <td>95</td>
                <td>275</td>
            </tr>
            <tr>
                <td>103</td>
                <td>Aman</td>
                <td>75</td>
                <td>80</td>
                <td>72</td>
                <td>227</td>
            </tr>
            <tr>
                <td>104</td>
                <td>Neha</td>
                <td>88</td>
                <td>91</td>
                <td>84</td>
                <td>263</td>
            </tr>
            <tr>
                <td>105</td>
                <td>Arjun</td>
                <td>79</td>
                <td>85</td>
                <td>81</td>
                <td>245</td>
            </tr>
        </tbody>

        <tfoot>
            <tr>
                <td colspan="2">Total Marks</td>
                <td>419</td>
                <td>422</td>
                <td>422</td>
                <td>1263</td>
            </tr>
            <tr>
                <td colspan="5">Average Total Marks per Student</td>
                <td>252.6</td>
            </tr>
        </tfoot>
    </table>

</body>
</html>

Submission

1. Save the HTML code as "marksheet.html".
2. Open the file in a web browser.
3. Check that all five students and the footer totals are visible.
4. Take a screenshot of the complete table and submit it with "Assignment-4.3.md".