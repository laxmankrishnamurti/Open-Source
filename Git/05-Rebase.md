# `Rebase`

- We can use the fature when we want to change the base of the branch.
- It means we are trying to move our branch to a new starting point.

```bash
git checkout <brach-name-except-main-or-master>
git merge master/main
```

Done.

The current branch is upto-dated with new main/master branch. That's it.

But, this creates an unnecessary commit which dosen't make any sense. To solve the problem _rebase_ comes into the picture.

## `Condition`

- We must ensure we are on the brach we want to rebase.
- Resolving conflict will be same as previous.

```bash
# Rebase the brach
git checkout <brach-name>
git rebase <main/master>
```

## `Git Reflog`

Git Reflog is a command that show us the history of our commits. It allows us to see the changes that we have made to our repository over time.

This can be useful for debugging and understanding the history of our project.

```bash
# All commits
git reflog

# Specific commit
git reflog <commit-hash>

# Hard-reset commit (carefully)
git reset --hard <commit-hash>

# Reset to the nth commit
git reset --hard HEAD@{<number>}
```
