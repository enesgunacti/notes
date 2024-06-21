# Basic Git Commands for Junior Developers

Welcome to your journey as a junior software developer! Below is a list of essential Git commands that you will use frequently. Git is a powerful version control system that helps you manage changes in your code and collaborate with others.

## Table of Contents
1. [Setup](#setup)
2. [Repository Initialization](#repository-initialization)
3. [Basic Workflow](#basic-workflow)
4. [Branching](#branching)
5. [Merging](#merging)
6. [Remote Repositories](#remote-repositories)
7. [Useful Commands](#useful-commands)

## Setup

### Configure Git
Before using Git, you need to set up your username and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## Repository Initialization

### Initialize a Repository
To start a new Git repository:

```bash
git init
```

### Clone an Existing Repository
To clone a repository from a remote source:

```bash
git clone <repository-url>
```

## Basic Workflow

### Check Repository Status
To see the current status of your working directory and staging area:

```bash
git status
```

### Add Changes to Staging
To add files to the staging area:

```bash
git add <file>
```

To add all changes:

```bash
git add .
```

### Commit Changes
To commit staged changes with a message:

```bash
git commit -m "Your commit message"
```

### View Commit History
To view the commit history:

```bash
git log
```

## Branching

### Create a New Branch
To create a new branch:

```bash
git branch <branch-name>
```

### Switch to a Branch
To switch to another branch:

```bash
git checkout <branch-name>
```

### Create and Switch to a New Branch
To create a new branch and switch to it immediately:

```bash
git checkout -b <branch-name>
```

## Merging

### Merge a Branch
To merge a branch into your current branch:

```bash
git merge <branch-name>
```

### Resolve Merge Conflicts
If there are conflicts during a merge, Git will notify you. You need to manually resolve them, add the resolved files, and then commit the merge:

```bash
# After resolving conflicts
git add <file>
git commit -m "Resolved merge conflicts"
```

## Remote Repositories

### Add a Remote Repository
To add a remote repository:

```bash
git remote add origin <remote-repository-url>
```

### View Remote Repositories
To view all configured remote repositories:

```bash
git remote -v
```

### Push Changes
To push changes to the remote repository:

```bash
git push origin <branch-name>
```

### Pull Changes
To pull changes from the remote repository:

```bash
git pull origin <branch-name>
```

## Useful Commands

### Discard Changes
To discard changes in your working directory:

```bash
git checkout -- <file>
```

### Remove Files
To remove files from the working directory and the staging area:

```bash
git rm <file>
```

### Rename Files
To rename a file:

```bash
git mv <old-filename> <new-filename>
```

### Stash Changes
To save changes temporarily:

```bash
git stash
```

### Apply Stashed Changes
To apply stashed changes:

```bash
git stash apply
```

## Conclusion

These are the basic Git commands that every junior developer should know. With these commands, you can manage your code effectively and collaborate with other developers. As you gain more experience, you'll learn more advanced Git features that will further enhance your workflow. Happy coding!


## Links

[Turkish]("https://www.youtube.com/watch?v=Ke26wrLhBHo&list=PLGrTHqyRDvx4WAg9LPX_GKk7cKF7KBXOg&index=5")

[English]("https://www.youtube.com/watch?v=8JJ101D3knE&t=703s")