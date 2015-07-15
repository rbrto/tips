# Overwrite pull

```sh
git fetch --all
git reset --hard origin/master
```

# List of all the files changed in a commit

```sh
git ls-tree --name-only -r <commit-ish>
```

# Git reset first commit

```sh
git update-ref -d HEAD
```

# List all the conflicted files

```sh
git diff --name-only --diff-filter=U
```

# Remove branches that have already been merged with master
```sh
git branch --merged | grep -v '\\*' | xargs -n 1 git branch -d
```