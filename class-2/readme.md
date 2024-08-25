### **For First-Time Setup**

1. **`git init` (Initialize the Repository):**
   - Initializes a new Git repository in your project directory, allowing Git to start tracking changes.

2. **`git add .` or `git add <file/folder name>` (Start Tracking Files):**
   - Stages files or folders to be included in the next commit.
   - `git add .` adds all files in the current directory.
   - `git add <file/folder name>` adds specific files or folders.

3. **`git commit -m "<message>"` (Commit Your Changes):**
   - Saves the changes you've staged with a descriptive message, marking a point in the project's history.

4. **`git remote add <origin name> <origin/repo URL>` (Link Your Local Repo to a Remote Repo):**
   - Links your local repository to a remote repository hosted on platforms like GitHub or GitLab.

5. **`git branch -m <branch name>` (Create or Rename a Branch):**
   - Renames the current branch or creates a new branch with the specified name, allowing you to work on different features separately.

6. **`git push -u <origin name> <branch name>` (Push Your Changes to the Remote Repository):**
   - Pushes your committed changes to the remote repository and sets the upstream tracking reference for future pushes.

### **For Updating Your Repository**

1. **`git add .` or `git add <file/folder name>` (Stage Your Updated Files):**
   - Stages your updated files or new files to be included in the next commit.

2. **`git commit -m "<new message>"` (Commit Your Changes with a New Message):**
   - Saves the staged changes with a new descriptive message.

3. **`git push <origin name> <branch name>` (Push Your Updates to the Remote Repository):**
   - Pushes your latest commits to the remote repository on the specified branch.

### **Summary of Commands**

#### **For First-Time Setup:**
```bash
git init
git add . or file/folder name
git commit -m "<message>"
git remote add <origin name> <origin/repo URL>
git branch -M <branch name>
git push -u <origin name> <branch name>
```

#### **For Updating Your Repository:**
```bash
git add . or file/folder name
git commit -m "<new message>"
git push <origin name> <branch name>
``` 