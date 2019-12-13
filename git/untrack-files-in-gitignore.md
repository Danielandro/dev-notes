# Untrack files already added to git repository based on .gitignore

Useful if you have already added/committed some files to your git repository and you then add them to your .gitignore.

These files will still be tracked by git as they were already commited.

## 1. Commit all your changes

First, make sure all changes are committed, including the .gitignore file.

## 2. Untrack all files from repository

To clear your repo, use:

`git rm -r --cached .`

- `rm` is the remove command
- `-r` will allow recursive removal
- `–cached` will only remove files from the index. The files will still be there.
- The `.` indicates that all files will be untracked. Specific files can be untracked with `git rm --cached foo.txt`

The rm command can be unforgiving. If you wish to try what it does beforehand, add the `-n` or `--dry-run` flag to test things out.

## 3. Re-track everything

`git add .`

## 4. Commit

`git commit -m ".gitignore fix"`

The repo is now clean :shower:

Push the changes to your remote to see the changes effective there as well.

---

[Main Page](../README.md)
