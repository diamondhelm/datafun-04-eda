# datafun-04-eda
## How to Install and Run the Project
# Step 1: Create a new repository in Github
Log in to GitHub.
Go to Profile>"Your repositories"
Click the "New" button OR in the top-right corner of GitHub>click the + dropdown menu>Select New repository.
Provide a brief description of your project.
Select the Public option so others can view my repository.
Add a Default README File by checkinh the box for Add a README file. The README file is essential for cloning and initializing a project.
Click Create the Repository to finalize the process.
# Step 2: Clone the Repository to my local machine and open in VS Code (ALWAYS use Git to clon)
Open Windows PowerShell
Type: "cd " to get to the root directory of the current drive. In this case it's C:\ (CD stands for change directory)
Copy repo url from GithHub: https://github.com/ssowers2/datafun-04-eda
Clone the repo by using git commands and pasting its url in the command line: git clone https://github.com/ssowers2/datafun-04-eda
Open VS Code>File>Open Folder>Select the new repo folder (don't double click it)>Click Select Folder
# Step 3: Add gitignore and requirements.txt files (if starting project from scratch)
Create new file in root project folder named: ".gitignore" If the name or location is not exact, it will not work.".gitignore" files are used to keep things out of GitHub like .venv and secrets
Find the .gitignore file in the root of this repo and paste the below contents as a starting point. Contents vary based on project:
This .gitignore file lists content that does NOT need to be tracked in the project history
# Python virtual environment folder
.venv/

# Visual Studio Code settings and workspace folder
.vscode/

# Compiled Python files
pycache/

# macOS system files
.DS_Store

# Jupyter Notebook checkpoint files
.ipynb_checkpoints

Create new file in root project folder named: "requirements.txt" If the name or location is not exact, it will not work. The contents in this fle will vary. Example: https://github.com/denisecase/pro-analytics-01/blob/main/requirements.txt.
# Step 4: git add, git commit -m "Message here", and git push -u orgin main
This is a good time to git-add-commit-push changes to the remote repository in GitHub
git add .- stages changes, adds files to source control
git commit -m "Initial commit"- creates a labeled snapshot of staged changes.
git push -u origin main - updates the remote repository
After subsequent changes, I can use a simpler version of the last command: git push
# Step 5: Set Up virtual environment for my local project (ALWAYS create a local virtual environment for project)
FYI: This is typically done once at the beginning of a project. If it gets messed up, delete .venv and recreate it. Never edit .venv directly. Explore the folder but leave the contents alone!

Open project repo folder in VS Code
Open terminal and make sure it's set to PowerShell
Create .venv by typing the command: py -m venv .venv
Activate .venv by typing the command. This is for Windows OS: .\.venv\Scripts\activate
Select VS Code interpreter to use .venv: Open the command palette (Ctrl Shift P) and search for "Python: Select Interpreter". Then, select the .venv folder in the project root directory.Now my editor will know about the code in my .venv.
# Step 6: Install dependencies into .venv that are required for the project
We do not need to install packages from the Python Standard Library - they are included with our version. The standard library includes helpful packages like pathlib, sqlite3, os, sys, time, and more. See the index.

External dependencies are libraries, packages, and modules beyond the standard library and include common packages like pandas, numpy, seaborn, and matplotlib. These must be installed into our local project virtual environment to use them in our code.

Open project repository in VS Code.
Open PowerShell terminal.
Activate the .venv (if not already): .\.venv\Scripts\activate
Install dependencies listed in requirements.txt file using command: py -m pip install -r requirements.txt
Example to install single dependency: pip install requests
Example how to install multiple at once (space between each dependency): pip install numpy pandas requests
# Step 7: Create a New Jupyter Notebook
Open project in VS Code: File>Open Folder and select project directory folder.
Ensure the Jupyter Extension is Installed: Go to Extensions (Ctrl+Shift+X)>Search for "Jupyter">If not installed, click Install on the Jupyter extension by Microsoft.
Click File>New File>Name file new_notebook.ipynb (or any name ending in .ipynb).
Press Enter, and VS Code will recognize it as a Jupyter Notebook.
Open and Edit the Notebook
Click on new .ipynb file. It will open in Notebook Editor mode. I will see a cell-based editor where I can write and execute Python code.
