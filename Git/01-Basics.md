# Basics

- Install Git on your local system
- Create an GitHub Account

- Git ===> Version control system
- GitHub ===> Cloud based service (Code hosting)

## `Terminology`

```bash
# Git version

git --version
```

- Repository (Folder/Directory)

```bash
# Git status

git status
```

### Configuration

```bash
git config --global user.email "YOUR EMAIL"
git config --global user.name "YOUR USERNAME"

git config --list
```

```bash
# Initialize a git repository

git status
git init (Tracking start)
```

- Flow
  - Initialize a repository
  - Write
  - Add (Staging area)
  - Commit (Enter into repo => Save locally => Check-point)
  - Push (To GitHub)

### Stage

```bash
git init

# Stage all files at once
git add .

# Stage files one by one by specifying their name
git add <filename>

git status
```

```bash
# unstage the changes

git rm --cached <fielname1> . . . .n
```

### Commit

```bash
# Message (like an instruction or command to a machine)

git commit -m "Meaningful message"
```

### Log

```bash
git log
git log --oneline
```

### Change Default code editor (vim)

- Install VS Code command line tool.

```bash
CTRL + SHIFT + P

# Search
Shell Command: Install 'code' command in PATH
```

OR Just run the code(latest version)

```bash
git config --global core.editor "code --wait"
```

### `gitignore`

```bash
# In the root directory

touch .gitignore

# To track empty files
touch .keep
```

Add files into the file to be ignored.
