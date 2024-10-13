# Git Tutorial

This guide covers essential and advanced Git commands for managing your codebase efficiently.

---

## Table of Contents

1. [Initialize a Repository](#git-initialize)
2. [Default Branch Setup](#default-branch-setup)
3. [Commit Status](#commit-status)
4. [Add Files and Folders](#add-files-and-folders)
5. [Commit Changes](#commit-changes)
6. [View Commit History](#view-commit-history)
7. [Branches](#branches)
8. [Merging Branches](#merging-branches)
9. [Remote Repositories](#remote-repositories)
10. [Pulling and Pushing Changes](#pulling-and-pushing-changes)
11. [Stashing Changes](#stashing-changes)
12. [Viewing Differences](#viewing-differences)
13. [Resetting and Reverting](#resetting-and-reverting)

---

## Git Initialize

To initialize a Git repository, run the `git init` command. This creates a `.git` folder that tracks your project’s history and changes.

```
git init
```

---

## Default Branch Setup

By default, the main branch may be called `master`. To change the default branch name (e.g., to `main`), run the following command:

```
git config --global init.defaultBranch main
```

---

## Commit Status

The `git status` command gives a summary of the current state of the repository. This includes:

- **Current branch**: Shows which branch you are working on.
- **Untracked files**: Files that are new and not yet tracked by Git.
- **Changes to be committed**: Files that have been staged for commit.
- **Unstaged changes**: Changes that have been made but not yet staged.

```
git status
```

---

## Add Files and Folders

Before committing changes, you need to add the files to the staging area.

```
# Add all files and folders
git add .

# Add a specific file
git add <filename>

# Add a specific folder
git add <foldername>/
```

---

## Commit Changes

Once the changes are added to the staging area, use the `git commit` command to commit them to the repository.

```
git commit -m "Your commit message"
```

You can also add files and commit at once:

```
git commit -am "Your commit message"
```

---

## View Commit History

To view the commit history of the repository, use:

```
git log
```

- `git log --oneline`: Shows a more concise log with one commit per line.
- `git log --graph`: Displays the commit history as a graph, useful for viewing branches.

---

## Branches

Git allows you to work on different versions of your project with branches. Here's how to create and switch branches:

```
# Create a new branch
git branch <branchname>

# Switch to another branch
git checkout <branchname>

# Create and switch to a new branch in one command
git checkout -b <branchname>
```

To list all branches:

```
git branch
```

- `*` indicates the branch you are currently on.

---

## Merging Branches

To merge the changes from one branch into another, switch to the branch you want to merge into and use the `git merge` command.

```
# Switch to the branch you want to merge into (e.g., main)
git checkout main

# Merge the feature branch into the main branch
git merge <branchname>
```

---

## Remote Repositories

To work with a remote repository (e.g., GitHub or GitLab), you'll need to link the local repository to the remote one.

```
# Add a remote repository
git remote add origin <remote-url>

# Verify the remote link
git remote -v
```

---

## Pulling and Pushing Changes

To fetch and integrate changes from the remote repository into your local repository, use:

```
git pull origin <branchname>
```

To send your local commits to the remote repository:

```
git push origin <branchname>
```

If you are pushing to a new branch for the first time:

```
git push -u origin <branchname>
```

---

## Stashing Changes

If you need to switch branches but have uncommitted changes, you can "stash" those changes temporarily:

```
git stash
```

To retrieve stashed changes:

```
git stash pop
```

To list all stashes:

```
git stash list
```

---

## Viewing Differences

You can view the changes between your working directory and the last commit, between commits, or between branches.

```
# View changes in the working directory (compared to last commit)
git diff

# View changes between two commits
git diff <commit1> <commit2>

# View changes between two branches
git diff <branch1> <branch2>
```

---

## Resetting and Reverting

Sometimes, you may want to undo changes. Git provides several commands to achieve this.

### Reset to a Specific Commit

```
# Soft reset (keeps your changes in the working directory)
git reset --soft <commit>

# Hard reset (discards all changes)
git reset --hard <commit>
```

### Revert a Commit

Reverting creates a new commit that undoes the changes made in a previous commit.

```
git revert <commit>
```

---

This concludes the detailed documentation on Git commands. These commands should cover most of the common Git operations, from setting up a repository to collaborating with others.
