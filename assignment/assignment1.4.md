1. Install Git and Verify Installation

Download Git from https://git-scm.com/downloads and install it.

Verify the installation using:

git --version

2. Open the Project Folder

Open the terminal in the project folder or run:

cd web-development-practice

3. Initialize the Git Repository

Run the command:

git init

This initializes a Git repository in the project folder.

4. Configure Git Username and Email

git config --global user.name "Your Name"
git config --global user.email "you@example.com"

Replace the example details with your own name and email address.

5. Create an HTML File

Create a file named "index.html" and add the following code:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Git Essentials I</title>
</head>
<body>
    <h1>Welcome to Git Essentials!</h1>
    <p>This is my first Git practice project.</p>
</body>
</html>

6. Check Repository Status

git status

This command shows the current state of files in the repository.

7. Make Three Meaningful Commits

Commit 1: Add the initial HTML page

git add index.html
git commit -m "Add initial HTML page"

Commit 2: Update the HTML page

Add a new paragraph to "index.html", save the file, and run:

git add index.html
git commit -m "Add introduction to webpage"

Commit 3: Add project documentation

Create a "README.md" file describing the project, then run:

git add README.md
git commit -m "Add project README"

8. View Commit History

git log --oneline

This command displays the commit history. At least three commits should appear.

9. Expected Folder Structure

web-development-practice/
├── .git/
├── index.html
└── README.md

10. Screenshots for Submission

1. Screenshot of the repository folder and its files.
2. Screenshot showing the Git version and repository status.
3. Screenshot showing the history of three commits using "git log --oneline".

Conclusion

This assignment helped me learn how to install and configure Git, initialize a repository, track changes, stage files, create meaningful commits, and view the commit history using terminal commands.