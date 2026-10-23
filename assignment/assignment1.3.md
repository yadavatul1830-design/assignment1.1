1. Create the Project Folder

Command:

mkdir web-development-practice
cd web-development-practice

2. Create Week Folders

Command:

mkdir week-1 week-2 week-3

3. Create index.html Files

Command:

touch week-1/index.html week-2/index.html week-3/index.html

For Windows PowerShell, use:

New-Item week-1/index.html, week-2/index.html, week-3/index.html -ItemType File

4. Practice Navigation

Commands:

cd week-1
cd ..
cd week-2
cd ..

These commands are used to move between folders and return to the parent folder.

5. Rename a Folder

Commands:

mv week-3 week-3-renamed
mv week-3-renamed week-3

These commands rename the folder and then restore its original name.

For Windows PowerShell:

Rename-Item week-3 week-3-renamed
Rename-Item week-3-renamed week-3

6. Delete a Folder

Commands:

mkdir temporary-practice
rmdir temporary-practice

These commands create and delete an empty practice folder.

7. Display the Final Folder Structure

Command:

tree

This command displays the folders and files in a tree structure.

8. Open the Project in Visual Studio Code

Command:

code web-development-practice

This command opens the project folder in Visual Studio Code when the "code" command is available.

9. Expected Final Folder Structure

web-development-practice/
├── week-1/
│   └── index.html
├── week-2/
│   └── index.html
└── week-3/
    └── index.html

Conclusion

This assignment helped me learn how to create folders and files, navigate between directories, rename and delete folders, display a folder structure, and open a project in Visual Studio Code using terminal commands.

Submission

Attach a screenshot of the terminal showing the final folder structure after running the commands on your computer.