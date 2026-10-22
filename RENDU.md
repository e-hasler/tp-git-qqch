# Rendu : e-hasler

- Dépôt : https://github.com/e-hasler/tp-git-qqch
- Site GitHub Pages : https://e-hasler.github.io/tp-git-qqch/

## Ex2
git log --oneline :
308054c (HEAD -> main, origin/main) ex2: corrige une faute
3079c07 ex2: crée les notes
abfdfe6 ex1: initialise le dépôt

## Ex3
- config.local est-il encore dans l'historique ? Pourquoi ?
Oui il y est encore car il a été commit au moins une fois avant d'être untracked. C'est à partir du moment où on arrête de le suivre que ses versions cessent d'être consultables.

## Ex4
- git status après avoir retiré brouillon.txt du staging :
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    ancien.txt
        renamed:    a-supprimer.txt -> nouveau.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   brouillon.txt

- Différence entre annuler une modification et retirer du staging ?
retirer du staging = git oublie la modification
annuler une modification = le ficher est modifié localement

## Ex6
- À quoi servent <<<<<<<, ======= et >>>>>>> ?
<<<<<<< et >>>>>>> délimitent la zone de conflit et ======= fait la différence entre la version actuelle et la version entrante qui génère le conflit

## Ex7
- git stash list (avant récupération) :
stash@{0}: WIP on main: 80e5bb5 Revert "ex7: ajoute une ligne par erreur"
- Pourquoi annuler un commit plutôt que l'effacer de l'historique ?
Si on annule un commit avec git revert, on crée un nouveau commit qui annule l'action du commit problématique donc le commit problématique est toujours visible dans notre historique pour un meilleur suivi (et pour éviter les conflits)
Si on fait git reset, on demande à git d'ignorer notre/nos dernier(s) commit(s) ce qui peut causer des conflits notamment si on travaille collaborativement

## Ex8
- git pull = git fetch + quoi ?
git pull = git fetch + git merge

## Ex10
git log --oneline --graph --all :
* 60cd8e8 (HEAD -> main, tag: v1.0, origin/main, origin/HEAD) repondre aux questions 1 - 7
* 2046eb0 correct RENDU
* 210963a (tag: rendu) ex10: complète le rendu
* 5c62a99 add link to my website
* 3dd5cf6 ex9: ajoute la page d'accueil
*   5aeec45 Merge pull request #1 from e-hasler/feature-contact
|\  
| * 80b1503 (origin/feature-contact, feature-contact) ex8: ajoute la page contact
|/  
* 3d2ccaa ex7: ajoute la ligne en cours
* 8fff74e commit changes sur RENDU.md pour pouvoir stash pop
* bcaaef2 découverte du template RENDU.md ^^'
| * 9b8d349 (refs/stash) WIP on main: 80e5bb5 Revert "ex7: ajoute une ligne par erreur"
|/| 
| * 611546b index on main: 80e5bb5 Revert "ex7: ajoute une ligne par erreur"
|/  
* 80e5bb5 Revert "ex7: ajoute une ligne par erreur"
* 9267c1b ex7: ajoute une ligne par erreur
*   f85dd8d ex6: résout le conflit du titre
|\  
| * 4f0a773 (origin/version-en) ex6: titre en anglais
* |   f3528f2 ex6: fusionne fr
|\ \  
| |/  
|/|   
| * 0072e10 (origin/version-fr) ex6: titre en français
|/  
*   d38298f ex5: fusionne feature-menu
|\  
| * 3be9cf3 (origin/feature-menu) ex5: ajoute un dessert
| * e8f4434 ex5: crée le menu
|/  
* e8fd3bd ex4: ajoute trois fichiers
* ef2a856 ex3: arrête de suivre config.local
* 8c1f12b ex3: arrête de suivre config.local
* 95ce52d ex3: ajoute config.local (erreur)
* 743b183 ex3: ajoute .gitignore
* 308054c ex2: corrige une faute
* 3079c07 ex2: crée les notes
* abfdfe6 ex1: initialise le dépôt


git config --global alias.lg "log --oneline --graph --all"
git tag -a v1.0 -m "mon message de tag annotation"   