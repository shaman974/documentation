# GIT

## Site officiel

https://git-scm.com/docs

## Exemple de ligne de commande

http://cheat.errtheblog.com/s/git

## Tuto git

### exemple de creation de repo

https://www.christopheducamp.com/2013/12/15/github-pour-nuls-partie-1/

https://www.christopheducamp.com/2013/12/16/github-pour-nuls-partie-2/

### supression commit

https://makina-corpus.com/blog/metier/archives/git-annuler-proprement-un-commit-apres-un-push

### Quelques commandes

faire un revert sur un commit
```
git revert <numeroCommit>
```

voir toutes les branches
```
git branch -a
```
supprimer une branche
```
git branch -d <nomBranche>
```
  
### Rebase

Modificier les 2 derniers Commit
```
git rebase -i HEAD~2
```
