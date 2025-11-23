# PythonCSE__project__filemanagementapp
📁 File Management CLI Application
A simple command-line interface (CLI) application built in Python for basic file management operations in the current working directory.

✨ Features
This application allows users to perform the following file operations:

Create File: Creates a new, empty file. It handles cases where the file already exists.

View All Files: Lists all files and directories in the current working directory.

Delete File: Permanently deletes a specified file. It handles cases where the file is not found.

Read File: Displays the content of a specified file. (Note: See ⚠️ Known Issues)

Edit File: Appends new content to a specified file. (Note: See ⚠️ Known Issues)

Exit: Terminates the application.

🛠️ Requirements
The application uses built-in Python modules and requires Python 3.x to run.

os module (used for viewing, deleting, and managing files/directories)

🚀 How to Run
Save the Code: Save the provided Python code as a file (e.g., file_manager.py).

Open Terminal: Navigate to the directory where you saved the file using your terminal or command prompt.

Execute: Run the application using the following command:

Bash

python file_manager.py
Use the Menu: Follow the on-screen menu prompts to select an operation (1 through 6).

💡 Code Structure
The application is structured into several functions, each handling a specific file operation, and a main loop to run the menu:

create_file(filename): Handles file creation using the 'x' mode to prevent overwriting.

view_all_files(): Lists files using os.listdir().

delete_file(filename): Deletes a file using os.remove().

read_file(filename): Reads file content.

edit_file(filename): Appends content to a file.

main(): The primary function containing the application loop and menu.

⚠️ Known Issues and Enhancements
Please note the following issues in the current code that should be addressed for full functionality:

Fixed Filename in read_file and edit_file:

The read_file and edit_file functions are currently hardcoded to operate on a file named 'smaple.txt' (note the typo) instead of using the filename argument passed to them by the main function. They should be corrected to use the variable passed in.

Incorrect Variable in edit_file call:

In the main function, when calling edit_file, it passes the undefined variable file instead of the user-inputted filename.

Unconditional break in main:

The break statement after calling edit_file causes the application to exit immediately after editing, which is likely unintended.
