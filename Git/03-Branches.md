# Branches

Branches are the one of the most powerful feature of Git. Git offers to create multiple branches in a same project. Branches are totally isolated from the _main_ branche and can works independently.

Means, it facilitates to work on multiple features at the same time in the same project.

## HEAD

Head is a pointer which points the tip of the current branch.

```bash
git branch
git branch <new-branch>
git switch <existing-branch-name>

# Create and switch to a new branch
git switch -c <branch-name>

# Checkout to existing branch
git checkout <branch-name>
```

When we create a new branch to the repository git creates a new _reference_ of the branch in the location:

```bash
.git/refs/heads/new-branch-name
```

And when we checkout to other branch, HEAD starts pointing to the current branch, like this:

```bash
ref: refs/heads/bug-fix
```

## `Merging`

Now, its time to merge or collect all work together that has been done. In merging, we collect all resources from different branches and merge it to the _main_ branch.

```bash
git checkout main/master

# Condition : main/master branch should not change after creating the branch
git merge <branch-name>
```

### `Not fast-forward merge`

All are same but the point is main branch is also in development phase. All other branches and the main branch itself is updating continuously, hence all have different kind of state.

```bash
# Keep in mind that the branch is not up-to dated with the main branch
git merger <branch-name>
```

### `Merge Conflicts`

Conflicts happens when we try to merge same file with different-different content.

There is no magic to solve merge conflicts we need to manually resolve the issue that we face while merging. The merger conflicts happens when we try to merge the same files with different content.

It means let say there is a file in the main branch and we have created a new-branch and start making changes in the same file in both branches and once it get done we try to merge the branch so we checkout to the main branch and run the command:

```bash
git merge <branch-name>
```

We'll see a conflict file is opened which we have to resolve it manually and then add it and then commit it.

```bash
git merge --abort
git merge <branch-name>
```

Resolve the conflict manually and then run the command:

```bash
git add <file-name>
git commit -m "<message>"
```

### `Useful command`

```bash
# Rename branch
git branch -m <old-brach-name> <new-branch-name>

# Delete branch
git branch -d <branch-name>

# Checkout to any existing branch
git checkout <branch-name>

# List all branches
git branch
```
