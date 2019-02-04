# Configuration
## Set username and email

```bash
# Globally
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
# In Repo
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
git reset <filename>
```

## Working with stash
```bash
git stash && git unstash
```

## Abort rebase
```bash
git rebase --abort
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
git commit --author "Carl Bäckström <carl.backstrom@smithmicro.com>"
```

## Reset a specific file
```
git checkout HEAD <my-file.txt>
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
git clean -xdf
```
-x ignored files
-d recursive
-f force

## Change remote URL
```bash
git remote set-url origin git@github.com:carlba/linuxconf.git
```

## Information about how to dig through git history
https://jfire.io/blog/2012/03/07/code-archaeology-with-git/
