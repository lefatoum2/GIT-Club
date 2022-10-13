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

## Commit
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

## Touch

```
touch names.txt
```

```
nano names.txt
```

## Clone

```
git clone URL
git clone /existing/project dental
```
## Remote

```
git remote add remote-name URL
git remote rm remote-name
```

## Pull
La commande git pull est utilisée pour faire un fetch du contenu d'un dépôt distant et pour le télécharger, puis pour mettre à jour immédiatement le dépôt local qui correspond à ce contenu.

```
git pull thunk latest-analysis
```
