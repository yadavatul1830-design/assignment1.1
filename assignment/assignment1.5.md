1. Create a GitHub Account

Visit https://github.com/ and create a new account or sign in to an existing account.

2. Create a New Public Repository

1. Click the + icon on GitHub.
2. Select New repository.
3. Enter the repository name: "web-development-practice".
4. Select Public.
5. Click Create repository.

3. Connect the Local Repository to GitHub

Open the terminal in the local project folder and run the following commands. Replace "YOUR-USERNAME" with your GitHub username.

git remote add origin https://github.com/YOUR-USERNAME/web-development-practice.git
git branch -M main

If you already have a remote named "origin", update it using:

git remote set-url origin https://github.com/YOUR-USERNAME/web-development-practice.git

4. Upload Files to GitHub

Stage and commit your project files if they have not already been committed.

git add .
git commit -m "Add web development practice files"

Push the local repository to GitHub:

git push -u origin main

Complete any authentication prompts from GitHub.

5. Add a New File and Push the Second Commit

Create a new file named "README.md" in the project folder and add the following content:

# Web Development Practice

This project is created to practise basic web development and Git commands.

## Technologies Used
- HTML
- CSS
- JavaScript
- Git and GitHub

Save the file and run:

git add README.md
git commit -m "Add project README"
git push origin main

This uploads the new file and its commit to GitHub.

6. Verify the Commit History

Open your public GitHub repository in a browser:

"https://github.com/YOUR-USERNAME/web-development-practice"

Click the commit history link to verify that your commits appear on GitHub.

You can also check the history from the terminal:

git log --oneline

7. Submission

Public GitHub Repository Link:

"https://github.com/YOUR-USERNAME/web-development-practice"

Replace "YOUR-USERNAME" with your actual GitHub username and submit the working public repository link.

Conclusion

This assignment helped me learn how to create a public GitHub repository, connect a local Git repository to GitHub, upload project files using "git push", add new files, and verify commit history online.