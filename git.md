# Description
# Configuration

## Set username and email

### Globally
```bash
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

### Repo specific
```bash
git config user.name "John Doe"
git config user.email johndoe@example.com
```

# Usage

## Remove commits (Keep changes)
```bash
git reset --soft HEAD~3
```

## Remove commits (Scrap changes)
```bash
git reset --hard HEAD~3
```

## Unstage file
```bash
git reset
```

## Stash currently modified files
```bash
git stash
```

## Merge to parent branch
Checkout the feature branch

```bash
git checkout feature-branch
git merge parent-branch
```
Taken from: http://git-scm.com/docs/git-stash

## Delete branch

```
git branch -d the_local_branch
```

## Commit as a certain user
```bash
git commit --author "Carl Backström <carl.backstrom@smithmicro.com>"
```

## Reset a specific file

```
git checkout HEAD <my-file.txt>
```

```
git checkout -- <my-file.txt>
```

## Push tags

```bash
git push --tags
```

## Reword merge commit message.

```bash
git commit --amend -m"<new message>"
```
## Clean up repo
```bash
git gc --auto
```

## Change remote URL
```bash
git remote set-url origin git@github.com:carlba/linuxconf.git
```

# Customization
