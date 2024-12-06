# `GitHub`

- It is a cloud-based repository hosting service.

[Basic Configuration](./01-Basics.md)

## `Setup SSH key and add to GitHub`

- Mroe secure
- Prevent to re-login again-&-again.

[Instructions](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

## `Commands`

```bash
# Stage
git add .

# Commit
git commit -m <message>
```

- Create a GitHub Reposiroty

```bash
# Rename branch
git brach -M main

# Check remote urls (fetch and push url)
git remote -v

# Add remote repository
git remote add <remote-name (origin : Recommende)> url

# Push local files to GitHub repository
git push origin main

# Set upstreams brach (link a brach whenever we make push command)
git push --set-upstream origin main
git push -u origin <brach-name>

git push (changes added to the main branch)
```
