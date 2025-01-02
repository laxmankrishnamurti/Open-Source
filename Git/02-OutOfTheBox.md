# Underlying concept of Git tracking system

- Every commit gets a unique SHA(hash code) Id used to track file changes.
- Every hash contain lots of data and it depends on its' previous one.

## `3-Pillers of Git`

1. Commit object (Unique SHA)
2. Tree Object (Reference to go back)
3. Blob Object (Actual code that git has be to saved)

Commit Object gives reference to ===> Tree Object ===> Blob Object

### `1. Commit Object`

Each commit of the project is stored in _.git_ directory in the form of a commit object contains the following information:

- Tree Object
- Parent Commit Object
- Author
- Commiter
- Commit message

### `2. Tree Object`

Tree object is a container for all the files and folders in the project. It contains information:

- File Mode
- File Name
- File Hash
- Parent Tree Object

Everything is stored as key-value pairs in the tree object.

### `3. Bloob Object`

Blob Object is present in the tree object and contains the actual file content. This is the place where the file content is stored.

- Commit
  - Tree
    - Blob
      - Actual Code

## Commands

```bash
# Log to get commit hash
git log

# Inside a commit object
git show -s --pretty=raw <commitHash>
```

```bash
# Output

tree d70489360da5172c99ebeb427b466249b534dcf4
parent 749022c20c39643519c628cab10da06f96faa04d (Previous one or Parent Hash)
author laxmankrishnamurti <freelancing.laxman@gmail.com> 1733004480 +0530
committer laxmankrishnamurti <freelancing.laxman@gmail.com> 1733004480 +0530

    track empty directory
```

```bash
# Inside a tree object

git ls-tree <TreeId>
```

```bash
# Output

100644 blob 2eea525d885d5148108f6f3a9a8613863f783d36    .gitignore
100644 blob 802c8d9edbcd00fce049bb16446133cf8c93b29a    fileOne.md
100644 blob 4856fe236dbdd59db2741de0235ae7db63c27a1a    fileTwo.md
040000 tree 29a422c19251aeaeb907175e9b3219a9bed6c616    images
```

```bash
# Grap Blob

git show <blob-id>
```
