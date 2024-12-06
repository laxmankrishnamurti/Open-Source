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
