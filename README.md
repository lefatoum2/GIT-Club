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
git merge intègre immédiatement la branche principale distante dans la branche principale locale.
```
git merge [branch]

git merge source destination
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
git pull origin master
```

## Checkout

```
git checkout main
```
```
git pull origin
## Annule les changements
git checkout -- .
```

## Push
```
git push remote-name branch-name
git push origin master
```

## Log

```
git log
```

## Status
```
git status
```
## Add

```
git status
git add sources.txt
```
## .gitignore
Permet d'ignorer certains fichiers. Les fichiers ignorés sont généralement des artefacts de build et des fichiers générés par la machine qui sont dérivés de votre dépôt source ou qui ne devraient pas être commités. Quelques exemples fréquents.

```
pdf
*.pyc
backup
```

## Clean

```
git clean -f backup.log 
```
## config
```
git config --list --local
```

## reset

```
git reset
```

## Restaurer une vieille version
```
git log -2 data/reporting.txt
ou 
git log data/reporting.txt
```

```
commit ab8883e8a6bfa873d44616a0f356125dbaccd9ea
Author: Author: Rep Loop <repl@datacamp.com>
Date:   Thu Oct 19 09:37:48 2017 -0400

    Adding graph to show latest quarterly results.

commit 2242bd761bbeafb9fc82e33aa5dad966adfe5409
Author: Author: Rep Loop <repl@datacamp.com>
Date:   Thu Oct 16 09:17:37 2017 -0400
```

```
git checkout 2242bd data/reporting.txt
```
