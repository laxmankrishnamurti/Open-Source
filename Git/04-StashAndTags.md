# `diff stash and Tags`

- The _git diff_ is an informative command that shows the difference between two commits.
- Git consider the changed versions of same file as two different files and then it gives names to these two files and shows the difference between them.

------- = Prev
+++++++ = Current

```bash
# This cmd will not show any changes made in the file A and file B.
git diff

# This cmd shows the changes between our last commit and the staging area (changes are staged and ready to be commited.)
git diff --staged

# Comparison between two branches
git diff <branch-one> <branch-two>

# Comparison between two specific commits
git diff <commit-hash-one> <commit-hash-two>
git diff <commit-hash-one>..<commit-hash-two>
```

## `Git Stash`

Stash is a temporary location where we can save our changes. It is useful when we want to make changes to a file but don't want to commit them yet. We can then come back to the file later and apply the changes.

```bash
# Store temporarly (like a stack)
git stash

# Name the stash
git stash save "name"

# Get stash list
git stash list

# Apply stash
git stash apply

# Apply the specific stash
git stash apply stash@{<number>}

# Apply and Drop the stash
git stash pop

# Drop the stash
git stash drop

# Apply stash to specific branch
git stash apply stash@{<number>} <branch-name>

# Clear the stash
git stash clear
```

## `Git Tags`

Tags are a way to mark a specific point in our repository. They are useful when we want to remember a specific version of our code or when we want to refer to a specific commit.

In short, Tags are like sticky notes that we can attach to our commits.

```bash
# Create a tag
git tag <tag-name>

# Create an annotated tag
git tag -a <tag-name> -m "<message or released version>"

# List all tags
git tag

# Tag a specific commit
git tag <tag-name> <commit-hash>

# Push tags to remote repository
git push origin <tag-name>

# Delete a tag
git tag -d <tag-name>

# Delete tag on remote repository
git push origin :<tag-name>
```
