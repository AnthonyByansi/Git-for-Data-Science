# Git Advanced Techniques

Git is a powerful version control system that allows developers to collaborate on code and track changes over time. While Git is easy to use for basic tasks, mastering its advanced techniques can greatly enhance your productivity and efficiency. In this article, we'll explore some of the most useful Git advanced techniques that you can use to take your Git skills to the next level.

## Rebase

Git rebase is a technique that allows you to apply a series of changes from one branch to another. Unlike merge, which creates a new commit that combines changes from two branches, rebase applies the changes from one branch to another in a linear fashion, resulting in a cleaner and more organized Git history. 

To perform a rebase, you first need to switch to the branch that you want to apply the changes to. Then, use the `git rebase` command followed by the name of the branch that contains the changes you want to apply. Git will then replay each commit from the other branch onto the current branch, one at a time. 

While rebase can be a powerful tool for managing Git history, it should be used with caution, as it can cause conflicts and overwrite existing changes.

## Interactive Rebase
The interactive rebase is a variation of the rebase command that allows you to selectively apply, modify, or delete commits from a branch's history. This can be useful for cleaning up your Git history, squashing multiple commits into a single commit, or reordering commits.

To perform an interactive rebase, use the `git rebase -i` command followed by the name of the branch that you want to modify. Git will then open a text editor that allows you to edit the list of commits in the branch's history.  You can then modify the commits by reordering them, squashing them together, or deleting them altogether.

## Cherry-pick
Cherry-pick is a Git command that allows you to apply a specific commit from one branch to another branch. This can be useful when you want to apply a specific fix or feature to a branch without merging the entire branch.
To cherry-pick a commit, first, switch to the branch that you want to apply the commit to. Then, use the `git cherry-pick` command followed by the commit hash of the commit that you want to apply. Git will then apply the changes from that commit to the current branch.


## Submodules

Submodules allow you to include one Git repository within another Git repository. This can be useful when you want to reuse code from an external library or when you want to keep related projects in a single repository.
To add a submodule to your Git repository, use the `git submodule add` command followed by the URL of the repository that you want to include.  Git will then create a new directory within your repository that contains a clone of the external repository.

## Git Hooks
Git hooks are scripts that are automatically executed by Git before or after certain events, such as committing or merging changes. Git hooks can be used to automate tasks, enforce coding standards, or perform tests.
Git comes with several built-in hooks, such as **pre-commit** and **post-merge** hooks. 
