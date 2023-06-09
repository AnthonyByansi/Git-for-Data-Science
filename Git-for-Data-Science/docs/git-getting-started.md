## Getting Started with Git

This document provides an introduction to Git version control system for data science projects. If you are new to Git, this guide will help you get started with the basics of Git and its terminology.

## What is Git?

Git is a distributed version control system that allows you to track changes in your files and collaborate with others on projects. Git keeps a history of all changes to a project, making it easy to revert to previous versions or collaborate with others on the same project.

## Installing Git

To get started with Git, you'll need to install it on your computer. Git is available for Windows, Mac, and Linux operating systems. You can download Git from the official Git website: https://git-scm.com/downloads.

After you have downloaded Git, you can check if it's installed correctly by opening a terminal window and typing `git --version`. If Git is installed, the version number will be displayed in the terminal.

## Basic Git Terminology
Before you start using Git, it's important to understand some basic terminology:

* **Repository**: A repository, or *repo* for short, is a collection of files that are tracked by Git. Repositories can be stored locally on your computer or on a remote server like GitHub.

* Commit: A commit is a snapshot of a repository at a particular point in time. Each commit has a unique identifier, called a hash, that allows you to reference it later.

* Branch: A branch is a version of a repository that diverges from the main codebase. Branches are useful for developing new features or experimenting with changes without affecting the main codebase.

* Merge: Merging is the process of combining two or more branches into a single branch. This is typically done when a feature is complete and needs to be integrated into the main codebase.

## Creating a Git Repository

To create a new Git repository, navigate to the directory where you want to store your files and run the command `git init`. This command will create a new repository in the current directory.

```shell
$ cd /path/to/my/project
$ git init
```
## Tracking Changes

Once you have a repository set up, you can start tracking changes to your files. To track changes, you first need to add the file to the staging area using the `git add` command. Once a file is in the staging area, you can commit the changes using the `git commit` command.
```bash
$ git add my_file.py
$ git commit -m "Added a new file"
```

## Working with Remote Repositories

To collaborate with others on a Git project, you'll need to work with remote repositories. GitHub is a popular remote repository hosting service that provides free Git hosting for open source projects. You can also use other Git hosting services like GitLab or Bitbucket.

To work with a remote repository, you first need to create a new repository on the hosting service of your choice. Once the repository is created, you can clone it to your local computer using the `git clone` command.
```shell
$ git clone https://github.com/username/my-project.git
```

## Conclusion

> This guide provided an introduction to Git and its basic terminology. You learned how to create a new Git repository, track changes to your files, and work with remote repositories. In the next section, we'll cover best practices for working with Git in a data science project.
