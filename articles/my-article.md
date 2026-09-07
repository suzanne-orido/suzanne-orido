What is Git?
Git is a distributed version control software system that is capable of managing versions of source code or data. It is often used to control source code by programmers who are developing software collaboratively.

Why is version control important?
It is a system that records every change made to a file or set of files over time so that you can recall specific versions later.
The importance of version control includes:

Safety Net: You can "undo" mistakes by rolling back to any previous version of your project if something breaks.
Teamwork: It allows multiple people to work on the same files simultaneously without overwriting each other's progress.
Organization: It eliminates messy file naming (like final_v2_new.doc) by keeping one clean version while storing the history in the background.
Branching: You can create "branches" to experiment with new ideas in isolation without risking the stability of the main project.
Documentation: Every change is saved with a note (commit message), creating a detailed history of who changed what and why.
How to push code to Github
To push your code to GitHub, you first need a repository (a project folder) hosted on their site. Here is the standard workflow using the terminal.

1. Initial Upload (New Repository)
Use this sequence to link a local project to a newly created GitHub repository.

- Create Remote Repository: On GitHub, create a new repository. Do not initialize with a README, .gitignore, or license if code already exists locally.

- Initialize Local Git: Navigate to the project root and execute: git init

- Stage Files: Add all files to the staging area: git add.

- Create First Commit: Record the snapshot: git commit -m "initial commit"

- Define Main Branch: Ensure the primary branch is named main: git branch -M main

- Link Remote URL: Connect the local repository to GitHub: git remote add origin <github-repo-url>

Execute Push: Upload the code and set the upstream reference: git push -u origin main

2. Standard Synchronization (Existing Repository)
Use this sequence for ongoing updates to a repository that is already linked.

Stage Specific Changes: git add <file-name> (or git add. for all changes)

Commit: git commit -m "description of changes"

Push: git push

How to pull code from GitHub
Code retrieval from GitHub is categorized into two primary operations: Initial Acquisition (Clone) and Synchronization (Pull).

1. Clone:
Used when the code doesn't exist on the local machine

Identify Repository URL: On the GitHub repository page, click the Code button and copy the URL (HTTPS or SSH).

Initialize Download: Open the terminal and execute: git clone <repository-url>

Result: Git creates a directory named after the repository, downloads all files, branches, and the full commit history, and configures the remote reference (origin).

2. Pull/Synchronization
Used to update an existing local repository with changes from Github
- Navigate to Directory: Enter the local project folder.

- Execute Update: Run the following command: git pull origin <branch-name> Example: git pull origin main

- Mechanism: This command executes two sub-operations:

Fetch: Downloads remote data without altering local files.

Merge: Integrates remote changes into the current active branch.

How to track changes using Git
Git tracks changes by managing data between three logical states: the Working Directory (unsaved changes), the Staging Area (prepared changes), and the Local Repository (permanent history).

1. Initialization
Activate Git tracking in a project directory: git init This creates a .git subdirectory to store metadata and object databases.

2. State Verification
Determine the current status of files: git status

- Untracked: New files unknown to Git.

- Modified: Tracked files with unsaved changes.

- Staged: Changes moved to the Index, ready for the next snapshot.

3. Change Preparation (Staging)
Select specific changes for inclusion in the next version:

Single file: git add <file-name>

All changes: git add .

Interactive (partial file): git add -p

4. Version Finalization (Commit)
Record the staged changes as a permanent snapshot: git commit -m "Direct description of change" Standard format: Use imperative mood (e.g., "Fix logic error" rather than "Fixed logic error").

5. Change Analysis Tools
Real-time Differences
Analyze modifications before staging or committing:

- Unstaged changes: git diff (Compares working directory to staging area)

- Staged changes: git diff --staged (Compares staging area to last commit)

Historical Review
Inspect the chronological record of changes:

- Summary list: git log --oneline

- Detailed patches: git log -p

- File-specific history: git log -- <file-path>

Line-Level Attribution
Identify when and by whom specific lines were altered: git blame <file-name>
