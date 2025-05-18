GitHub et ses Commandees
============
*Git est le système de contrôle de version distribué, libre et open source, qui gère tout ce qui se passe localement sur votre ordinateur et qui concerne GitHub. Cet aide-mémoire présente les Commandees Git les plus importantes et les plus courantes pour une référence facile.*


## Versions traduites
- [English Version](README.md)
- [Türkçe Versiyon](READMEtr.md)
- [Versión en español](READMEes.md)


### INSTALLATION ET GUI
_Avec des installateurs spécifiques à la plate-forme pour Git, GitHub offre également la possibilité de rester à jour avec les dernières versions de l'outil de ligne de Commandee tout en fournissant une interface utilisateur graphique pour l'interaction quotidienne, la révision et la synchronisation du référentiel._

#### GitHub pour Windows
_htps://windows.github.com_

#### GitHub pour Mac
_htps://mac.github.com_

_Pour les plateformes Linux et Solaris, la dernière version est disponible sur le site Web officiel de Git._

#### GitHub pour toutes les plateformes
_htp://git-scm.com_

### INSTALLATION
_Configuration des informations utilisateur utilisées dans tous les référentiels locaux_

| Installation |
|-------|
|`git config --global user.name “[prénom nom]”` <br/> Définissez un nom identifiable pour le crédit lors de la révision de l'historique des versions|
|`git config --global user.email “[email-valide]”` <br/> Définissez une adresse e-mail qui sera associée à chaque marqueur d'historique|
|`git config --global color.ui auto` <br/> Définir la coloration automatique de la ligne de Commandee pour Git pour une révision facile|

### SETUP & INIT
_Configuration des informations utilisateur, initialisation et clonage des référentiels_

| Commande | Description |
| ------- | ----------- |
| `git init` | Initialize an existing directory as a Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Retrieve an entire repository from a hosted location via URL |

### STAGE & SNAPSHOT
_Working with snapshots and the Git staging area_

| Commande | Description |
| ------- | ----------- |
| `git status` | Afficher les fichiers modifiés dans le répertoire de travail, préparés pour votre prochain commit |
| `git add [file-name.txt]` | Ajoutez un fichier tel qu'il apparaît actuellement à votre prochain commit (étape) |
| `git add -A` | Ajoutez tous les fichiers nouveaux et modifiés à la zone de préparation |
| `git commit -m "[commit message]"` | Validez votre contenu mis en scène en tant que nouvel instantané de validation |
| `git reset [file]` | Annuler la mise en scène d'un fichier tout en conservant les modifications dans le répertoire de travail |
| `git diff` | Différence entre ce qui est modifié mais pas mis en scène |
| `git diff --staged` | Différence entre ce qui est mis en scène mais pas encore validé |
| `git rm -r [file-name.txt]` | Supprimer un fichier (ou un dossier) |
| `git remote -v` | Afficher le référentiel distant du fichier ou du répertoire en cours de travail |

### BRANCH & MERGE
_Isoler le travail dans les branches, changer le contexte et intégrer les changements_

| Commande | Description |
| ------- | ----------- |
| `git branch` | Lister les branches (l'astérisque indique la branche actuelle) |
| `git branch -a` | Lister toutes les branche (locales et distantes) |
| `git branch [branch name]` | créer une nouvelle branche au niveau du commit actuel |
| `git branch -d [branch name]` | Supprimer une branche |
| `git push origin --delete [branch name]` | Supprimer une remote branche |
| `git checkout -b [branch name]` | Créez une nouvelle branche et basculez vers celle-ci |
| `git checkout -b [branch name] origin/[branch name]` | Cloner une branche distante et y basculer |
| `git branch -m [old branch name] [new branch name]` | Renommer une branche locale |
| `git checkout [branch name]` | Passer à une branche |
| `git checkout -` | Passer à la dernière branche extraite |
| `git checkout -- [file-name.txt]` | Annuler les modifications apportées à un fichier |
| `git merge [branch name]` | Fusionner l’historique de la branche spécifiée dans celui actuel |
| `git merge [source branch] [target branch]` | Fusionner une branche dans une branche cible |
| `git stash` | Cacher les modifications dans un répertoire de travail sale |
| `git stash clear` | Supprimer toutes les entrées stockées |
| `git stash pop` | Appliquer la dernière réserve au répertoire de travail |
| `git log` | Afficher tous les commits dans l'historique de la branche actuelle |

### Sharing & Updating Projects
_Retrieving updates from another repository and updating local repos_

| Commande | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |
| `git fetch [alias]` | Fetch down all the branches from that Git remote |

### Inspection & Comparison
_Examining logs, diffs and object information_

| Commande | Description |
| ------- | ----------- |
| `git log` | Show the commit history for the currently active branch |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |
| `git log branchB..branchA` | Show the commits on branchA that are not on branchB |
| `git log --follow [file]` | Show the commits that changed file, even across renames |
| `git diff branchB...branchA` | Show the diff of what is in branchA that is not in branchB |
| `git show [SHA]` | Show any object in Git in human-readable format |

### TRACKING PATH CHANGES
_Versioning file removes and path changes_

| Commande | Description |
| ------- | ----------- |
| `git rm [file]` | Delete the file from project and stage the removal for commit |
| `git mv [existing-path] [new-path]` | Change an existing file path and stage the move |
| `git log --stat -M` | Show all commit logs with indication of any paths that moved |

### REWRITE HISTORY
_Rewriting branches, updating commits and clearing history_

| Commande | Description |
| ------- | ----------- |
| `git rebase [branch]` | Apply any commits of current branch ahead of specified one |
| `git reset --hard [commit]` | Clear staging area, rewrite working tree from specified commit |

### IGNORING PATTERNS
_Preventing unintentional staging or commiting of files_

| Commande | Description |
| ------- | ----------- |
| `logs/`<br/>`*.notes`<br/>`pattern*/` | Save a file with desired paterns as .gitignore with either direct string matches or wildcard globs. |
| `git config --global core.excludesfile [file]` | System wide ignore patern for all local repositories |

### TEMPORARY COMMITS
_Temporarily store modified, tracked files in order to change branches_

| Commande | Description |
| ------- | ----------- |
| `git stash` | Save modified and staged changes |
| `git stash list` | List stack-order of stashed file changes |
| `git stash pop` | Write working from top of stash stack |
| `git stash drop` | Discard the changes from top of stash stack |