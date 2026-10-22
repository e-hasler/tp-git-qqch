# Rendu : e-hasler

- Dépôt : tp-git-qqch
- Site GitHub Pages :

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

## Ex8
- git pull = git fetch + quoi ?

## Ex10
git log --oneline --graph --all :