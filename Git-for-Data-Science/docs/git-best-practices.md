# Git Best Practices

Version control systems are essential for any DataScience  project, and Git has become the de facto standard in recent years. However, using Git effectively requires some best practices to be followed, to avoid common pitfalls and ensure a smooth development process.

Here are some advanced Git best practices to take your workflow to the next level.

##  Use Git Hooks
Git hooks allow you to run custom scripts before or after certain Git actions, such as committing, pushing, or merging. This can be useful for enforcing coding standards, running automated tests, or generating documentation. You can find many pre-written hooks on GitHub, or write your own to suit your project's needs.

To set up a Git hook, create a script in the `.git/hooks` directory of your repository and make it executable.
**For example, to run a pre-commit hook that checks the code for syntax errors using `eslint`, create a file called `.git/hooks/pre-commit` with the following content:**

```bash
#!/bin/sh
npm run lint
```
Then make it executable with the following command: `chmod +x .git/hooks/pre-commit`
Now, every time you try to commit changes, the `npm run lint` command will be run automatically, and the commit will be aborted if there are any syntax errors.

## Use Git aliases
Git aliases allow you to create custom shortcuts for frequently used Git commands. This can save you a lot of time and typing, especially for complex commands with many arguments. You can set up aliases for any Git command, or even for custom scripts or external commands.

To set up a Git alias, use the `git config` command with the `alias.<name>` syntax, where `<name>` is the name of your alias.
For example, to create an alias called `s` for the `status` command, run the following command:`git config --global alias.s status`

Now you can run `git s` instead of `git status` to get the same output.

You can also create more complex aliases with arguments or options. For example, to create an alias called `hist` that shows a concise commit history with one-line summaries, run the following command: `git config --global alias.hist "log --pretty=format:'%h %s [%an]' --graph"`

Now you can run `git hist` to get a compact commit history with graph visualization and author names.

## Use Git Workflows
Git workflows are a set of guidelines for collaborating on a project using Git. They provide a clear structure for branching, merging, and releasing code, and help prevent conflicts and errors.

There are many Git workflows to choose from, depending on the size and complexity of your project. Some popular workflows include:
* Gitflow: A branching model that uses two main branches, `master` and `develop`, to manage releases and features respectively.
* GitHub Flow: A simple workflow that uses a single `master` branch and feature branches for development, with continuous integration and deployment.
* Trunk-based Development: A continuous integration and delivery workflow that uses a single `trunk` branch, with feature toggles and short-lived feature branches.

## Use Git Submodules
Git submodules allow you to include another Git repository as a subdirectory of your main repository. This can be useful for including shared libraries, dependencies, or plugins in your project, while still keeping them separate and version-controlled.

To add a submodule to your repository, use the `git submodule add` command followed by the URL of the repository you want to include.

For example, to add the `jquery` library as a submodule in your project, run the following command: `git submodule add https://github.com/jquery/jquery.git`

This will create a new directory called `jquery` in your repository, containing a clone of the `jquery` repository.

To update the submodule to the latest version, use the git submodule update command. `git submodule update --remote`

This will update the `jquery` submodule to the latest version available on the remote repository.
