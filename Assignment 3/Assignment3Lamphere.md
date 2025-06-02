# Git Configurations

## 1. What are the commands to configure your user.name and your user.email. Should this be configured globally or in your repo. Why or why not?
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```
You should configure these globally so Git knows the user identity across all repos, but locally can be used in times when muliple identities are needed.

## 2. How do you configure the core editor for git?
```bash
git config --global core.editor "code --wait"
```
This will set VS Code as the default editor. You can change it to other Git editors, like Vim by adding this...
```bash
git config --global core.editor "vim"
```

## 3. How do you view your global and local config?
```bash
git config --global --list   # Global settings
git config --local --list    # Local settings for current repo
```

# Working with a Local Repo

## 4. What are the steps to create a new local repo via the CLI?
```bash
mkdir new-local-repo
cd new-local-repo
git init
```

## 5. How do you clone a repo and what's the difference between cloning and creating a new repo from scratch? 
```bash
git clone https://github.com/octocat/Hello-World.git
```
Cloning a repo makes a copy of it for you locally. The difference between copying and creating a repo is a copy comes with all files, code, and branches. Whilst the new repo is a blank slate.

## 6. How do you look at the status of your repo? What information does this give you?
```bash
git status
```
This shows you the current branch, staged and unstaged changes, and files that are ready to commit.

## 7. How do you stage changes to your local repo in prepartion for a commit?
```bash
git add filename.txt     # stage one file
git add .                # stage all changes
```

## 8. How do you commit changes to your local repo?
```bash
git commit -m "Added new feature"
```

## 9. Include an example of a file that will allow you to "ignore" files in your repo. What kinds of files should not be part of your version control?
```bash
# Ignore node_modules and OS-specific files
node_modules/
.DS_Store
Thumbs.db
*.log
.env
```
The types of files that are ignored are those that are auto-generated local-only files.

## 10. How do you delete files using Git?
```bash
git rm filename
git commit -m "Delete filename"
```

# Working with a Remote
## 11 How do you view the remote repo that is associated with your local repo?
```bash
git remote -v
```

## 12. What is the function of the git fetch command?
```bash
git fetch
```

## 13. 13. What is the difference between fetch and pull?
```bash
git fetch
```
This is used to review changes before merging
```bash
git pull
```
This is a fetch and a merge within one command.

## 14. Make some changes in your repo and using the command line to sync those changes with your remote repo. Show the results.

```bash
# Stage the folder containing the assignment
git add "Assignment 3"

# Commit the new folder
git commit -m "Add Assignment 3 folder with markdown file"
```
```bash
PS C:\Users\TheAl\msse642-2025summer> git add "Assignment 3"
PS C:\Users\TheAl\msse642-2025summer> git commit -m "Add Assignment 3 folder with markdown file"
[main 84029b8] Add Assignment 3 folder with markdown file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Assignment 3/Assignment3Lamphere.md
PS C:\Users\TheAl\msse642-2025summer> git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 422 bytes | 422.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/SpencerLamphere/msse642-2025summer.git
   748d9b9..84029b8  main -> main
```

# Branches

## 15. How do you view the local and the remote branches for your repositories?
```bash
git branch        # local branches
git branch -r     # remote branches
git branch -a     # all branches
```

## 16. View and create a new branch
View:
```bash
PS C:\Users\TheAl\msse642-2025summer> git branch
# * main
```
Create:
```bash
PS C:\Users\TheAl\msse642-2025summer> git branch feature-branch
```
After:
```bash
PS C:\Users\TheAl\msse642-2025summer> git branch
  feature-branch
# * main
```

## 17. What are different ways to switch to a new branch?
```bash
git checkout feature-branch
```
or
```bash
git switch feature-branch
```

## 18. Delete your local branch without pushing to a remote or merging to your main branch. Show that it's gone.
```bash
PS C:\Users\TheAl\msse642-2025summer> git branch
  feature-branch
# * main
PS C:\Users\TheAl\msse642-2025summer> git branch -D feature-branch
Deleted branch feature-branch (was 84029b8).
PS C:\Users\TheAl\msse642-2025summer> git branch
# * main
```