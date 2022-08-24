# GIT-Club
GIT cheat sheet

Charger un projet:
```
git init
git remote add origin git@github.com:<user>/<repo>.git
git remote -v
git pull origin master
```

```
git init
git remote add origin <url>
git add .
git commit -m "Initial commit"
git push -u origin master
```
Configuration initiale:
```
git config --global user.name “[firstname lastname]”
```

```
git config --global user.email “[valid-email]”
```

```
git config --global color.ui auto
```

```
git status
```
```
git add [file]
```
```
git reset [file]
```

## Diff
```
git diff
git diff data/northern.csv
git diff -r HEAD data/northern.csv
```
```
git diff --staged
```
```
git commit -m “[descriptive message]”
```
```
git reset HEAD <file>

```

## Branch

```
git branch
```

```
git branch [branch-name]
```

```
git checkout

```
## Merge

```
git merge [branch]
```

```
git log
```
