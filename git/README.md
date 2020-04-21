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

Ajouter des modification à un commit non pushé
```
git commit --amend
```

Voir les logs
```
git log
```

Voir le delta de log
```
git log origin/develop..develop
```

### Rebase

Modificier les 2 derniers Commit
```
git rebase -i HEAD~2
```

https://git-scm.com/book/fr/v2/Utilitaires-Git-R%C3%A9%C3%A9crire-l%E2%80%99historique

```
# Commandes :
#  p, pick <commit> = utiliser le commit
#  r, reword <commit> = utiliser le commit, mais reformuler son message
#  e, edit <commit> = utiliser le commit, mais s'arrêter pour le modifier
#  s, squash <commit> = utiliser le commit, mais le fusionner avec le précédent
#  f, fixup <commit> = comme "squash", mais en éliminant son message
#  x, exec <commit> = lancer la commande (reste de la ligne) dans un shell
#  b, break = s'arrêter ici (on peut continuer ensuite avec 'git rebase --continue')
#  d, drop <commit> = supprimer le commit
#  l, label <label> = étiqueter la HEAD courante avec un nom
#  t, reset <label> = réinitialiser HEAD à label
#  m, merge [-C <commit> | -c <commit>] <label> [# <uniligne>]
#          créer un commit de fusion utilisant le message de fusion original
#          (ou l'uniligne, si aucun commit de fusion n'a été spécifié).
#          Utilisez -c <commit> pour reformuler le message de validation.
#
# Vous pouvez réordonner ces lignes ; elles sont exécutées de haut en bas.
#
# Si vous éliminez une ligne ici, LE COMMIT CORRESPONDANT SERA PERDU.
#
# Cependant, si vous effacez tout, le rebasage sera annulé.
```

#### Exemple : modifier un commit intermediaire non pushé

Commit A puis Commit B, on veut modifier le commit A (ammend non possible directement sinon modifie le B)

```
git rebase -i HEAD~2
```

Affiche
```
pick xxx commit A
pick yyy commit B
```

Modifier
```
edit xxx commit A
pick yyy commit B
```
```
Vous pouvez corriger le commit maintenant, avec

  git commit --amend

après avoir réalisé vos modifications, lancez

  git rebase --continue
```

Le source se retrouve à l'état juste apres le commit A avant le commit B
Modifer le source souhaité

Ajouter les modifications au commit A
```
git commit --amend
```

Réappliquer le commit B

```
git rebase --continue
```

