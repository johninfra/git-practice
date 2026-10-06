# Git Basics Practice

This file contains basic Git commands and notes I am practicing.

## Check Repository Status

```bash
git status
```

Shows which files are:

- Untracked
- Modified
- Staged
- Ready to commit

## Stage a File

```bash
git add filename
```

Example:

```bash
git add README.md
```

Stage all changes:

```bash
git add .
```

## Create a Commit

```bash
git commit -m "Commit message"
```

Example:

```bash
git commit -m "Add Git basics notes"
```

## View Commit History

```bash
git log
```

Short version:

```bash
git log --oneline
```

## View Changes

```bash
git diff
```

Shows changes that have not been staged yet.

To view staged changes:

```bash
git diff --staged
```

## Remove a File From the Staging Area

```bash
git restore --staged filename
```

Example:

```bash
git restore --staged README.md
```

## Restore Changes to a File

```bash
git restore filename
```

Warning: this removes uncommitted changes in that file.

## View Current Branch

```bash
git branch
```

The active branch will have an asterisk next to it.

Example:

```text
* main
```

## Push Changes to GitHub

```bash
git push
```

## Pull Changes From GitHub

```bash
git pull
```

## Basic Git Workflow

1. Make changes to files.

2. Check the changes:

```bash
git status
```

3. Stage the changes:

```bash
git add .
```

4. Commit the changes:

```bash
git commit -m "Describe the change"
```

5. Push the commit to GitHub:

```bash
git push
```

## Practice Goal

I want to become comfortable using Git from the terminal instead of relying only on the VS Code interface.