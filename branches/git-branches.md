# Git Branches Practice

This file contains notes and commands for practicing Git branches.

## What Is a Branch?

A branch is an independent line of development inside a Git repository.

Branches let you work on changes without directly affecting the main branch.

The default branch is usually:

```bash
main
```

## View Existing Branches

```bash
git branch
```

The current branch will have an asterisk next to it.

Example:

```text
* main
```

## Create a New Branch

```bash
git branch branch-name
```

Example:

```bash
git branch feature-test
```

## Switch to a Branch

```bash
git switch branch-name
```

Example:

```bash
git switch feature-test
```

Older Git syntax:

```bash
git checkout feature-test
```

## Create and Switch to a New Branch at the Same Time

```bash
git switch -c branch-name
```

Example:

```bash
git switch -c add-notes
```

This creates the branch and immediately switches to it.

## Check Which Branch I Am On

```bash
git branch
```

Example:

```text
  main
* add-notes
```

This means I am currently working on the `add-notes` branch.

## Make Changes on a Branch

After switching to a branch, edit or create files.

Then check the changes:

```bash
git status
```

Stage them:

```bash
git add .
```

Commit them:

```bash
git commit -m "Add changes on feature branch"
```

## Switch Back to Main

```bash
git switch main
```

## Merge a Branch Into Main

First switch to `main`:

```bash
git switch main
```

Then merge the branch:

```bash
git merge branch-name
```

Example:

```bash
git merge add-notes
```

This brings the committed changes from `add-notes` into `main`.

## Delete a Branch After Merging

```bash
git branch -d branch-name
```

Example:

```bash
git branch -d add-notes
```

The `-d` option safely deletes a branch after it has been merged.

## Force Delete a Branch

```bash
git branch -D branch-name
```

Warning: this can delete a branch even if its changes have not been merged.

## Push a Branch to GitHub

```bash
git push -u origin branch-name
```

Example:

```bash
git push -u origin add-notes
```

The `-u` option connects the local branch to the remote GitHub branch.

After that, future pushes can usually use:

```bash
git push
```

## View Local and Remote Branches

```bash
git branch -a
```

## Rename the Current Branch

```bash
git branch -m new-branch-name
```

## Basic Branch Workflow

1. Make sure the main branch is current.

```bash
git switch main
git pull
```

2. Create a new branch.

```bash
git switch -c feature-test
```

3. Make changes to files.

4. Check the changes.

```bash
git status
```

5. Stage the changes.

```bash
git add .
```

6. Commit the changes.

```bash
git commit -m "Add feature test"
```

7. Push the branch to GitHub.

```bash
git push -u origin feature-test
```

8. Switch back to main.

```bash
git switch main
```

9. Merge the branch.

```bash
git merge feature-test
```

10. Push the updated main branch.

```bash
git push
```

11. Delete the old local branch if it is no longer needed.

```bash
git branch -d feature-test
```

## Practice Exercise

Create a test branch:

```bash
git switch -c branch-practice
```

Create a file:

```bash
touch branch-test.txt
```

Add some text to the file, then run:

```bash
git status
git add .
git commit -m "Add branch practice file"
```

Switch back to main:

```bash
git switch main
```

Merge the practice branch:

```bash
git merge branch-practice
```

Then delete the branch:

```bash
git branch -d branch-practice
```

## Key Concept

Branches let me safely develop, test, and organize changes without immediately modifying the main version of a project.

A common workflow is:

```text
main
  |
  └── feature-branch
        |
        ├── make changes
        ├── commit changes
        └── merge back into main
```

## Practice Goal

I want to become comfortable creating branches, switching between them, making isolated changes, merging them back into main, and pushing branches to GitHub.