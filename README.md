# GIT-Club

![maxresdefault](https://user-images.githubusercontent.com/73175706/197197990-23bd9bc5-f337-4570-b90c-c529c230a533.jpg)

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

## Git Rebase

La commande "git rebase" est très utile quand une branche est toujours en développement alors qu'une mise en production a été faite.
En effet, dans ce cas, la branche "master" depuis laquelle la branche en cours de développement a été créée ne correspond plus au nouvel état de cette même branche "master". Dès lors, il faut "déplacer" les commits de ladite branche en développement pour les faire pointer sur le master actuel.
Pour cela, il faut utiliser la commande "git rebase".

 

Exemple : application d'un "rebase" sur la branche "master" pour la branche "mabranche" : 

### 1. Il faut d'abord se positionner sur la branche "master" pour la mettre à jour : 
```git
git checkout master
git remote update -p
git pull
```
### 2. après, il faut aller sur la branche "mabranche"
```
git checkout mabranche
```
### 3. on lance ensuite le rebase sur la branche "master"
```
git rebase master
```
### 4. le rebase indique une potentielle liste de conflits qu'il faudra résoudre avant d'aller plus loin. PHPStorm propose un excellent outil pour résoudre ces conflits.

### 5. pour chaque conflit résolu, ajouter le fichier correspondant (il est ajouté automatiquement avec l'outil de résolution de conflits de PHPStorm)
```
git add nom_du_fichier_qui_posait_problème
```
### 6. continuer le rebase (attention, il n'y a jamais de commit à faire malgré les "git add" à répétition)
```
git rebase --continue
```
### 7. quand le rebase est fini, il faut pousser la nouvelle branche en forçant la main à Git (car la nouvelle réorganisation des commits ne plaisant pas à Git, sans le -f, il ne voudra pas la faire)
```
git push -f origin mabranche
```
### 8. le rebase est fini.
