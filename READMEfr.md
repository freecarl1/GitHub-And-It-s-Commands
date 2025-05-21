GitHub et ses Commandees
============
*Git est le système de contrôle de version distribué, libre et open source, qui gère tout ce qui se passe localement sur votre ordinateur et qui concerne GitHub. Cet aide-mémoire présente les Commandees Git les plus importantes et les plus courantes pour une référence facile.*


## Versions traduites
- [English version (original)](README.md)
- [Türkçe Versiyon](READMEtr.md)
- [Versión en español](READMEes.md)


### INSTALLATION ET GUI
_Avec des installateurs spécifiques à la plate-forme pour Git, GitHub offre également la possibilité de rester à jour avec les dernières versions de l'outil de ligne de Commandee tout en fournissant une interface utilisateur graphique pour l'interaction quotidienne, la révision et la synchronisation du référentiel._

#### GitHub pour Windows
_https://windows.github.com_

#### GitHub pour Mac
_https://mac.github.com_

_Pour les plateformes Linux et Solaris, la dernière version est disponible sur le site Web officiel de Git._

#### GitHub pour toutes les plateformes
_http://git-scm.com_

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
_Récupération des mises à jour d'un autre repository et mise à jour des repository locaux_

| Commande | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Poussez une branche vers votre référentiel distant |
| `git push -u origin [branch name]` | Transférer les modifications vers le référentiel distant (et mémoriser la branche) |
| `git push` | Transférer les modifications vers le référentiel distant (branche mémorisée) |
| `git push origin --delete [branch name]` | Supprimer une branche remote |
| `git pull` | Mettre à jour le repository local avec le commit le plus récent |
| `git pull origin [branch name]` | Extraire les modifications du référentiel distant |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Ajouter un référentiel distant |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Définir la branche d'origine d'un référentiel sur SSH |
| `git fetch [alias]` | Récupérer toutes les branches de cette télécommande Git |

### Inspection & Comparison
_Examining logs, diffs and object information_

| Commande | Description |
| ------- | ----------- |
| `git log` | Afficher l'historique des commits pour la branche actuellement active |
| `git log --summary` | Afficher les modifications (détaillées) |
| `git log --oneline` | Afficher les modifications (brièvement) |
| `git diff [source branch] [branche cible]` | Prévisualiser les modifications avant la fusion |
| `git log branchB..branchA` | Afficher les commits sur la branche A qui ne sont pas sur la branche B |
| `git log --follow [file]` | Afficher les commits qui ont modifié le fichier, même après les renommages |
| `git diff branchB...branchA` | Afficher la différence entre ce qui est dans la branche A et ce qui n'est pas dans la branche B |
| `git show [SHA]` | Afficher n'importe quel objet dans Git dans un format lisible par l'homme |

### TRACKING PATH CHANGES
_Versioning file removes and path changes_

| Commande | Description |
| ------- | ----------- |
| `git rm [file]` | Supprimez le fichier du projet et organisez la suppression pour la validation |
| `git mv [existing-path] [new-path]` | Modifier un chemin de fichier existant et organiser le déplacement |
| `git log --stat -M` | Afficher tous les journaux de validation avec indication de tous les chemins déplacés |

### REWRITE HISTORY
_Réécriture des branches, mise à jour des commits et effacement de l'historique_

| Commande | Description |
| ------- | ----------- |
| `git rebase [branch]` | Appliquer tous les commits de la branche actuelle avant celui spécifié |
| `git reset --hard [commit]` | Effacer la zone de préparation, réécrire l'arborescence de travail à partir de la validation spécifiée |

### IGNORING PATTERNS
_Prévenir la mise en scène ou la validation involontaire de fichiers_

| Commande | Description |
| ------- | ----------- |
| `logs/`<br/>`*.notes`<br/>`pattern*/` | Enregistrez un fichier avec les modèles souhaités sous le nom .gitignore avec des correspondances de chaîne directes ou des globs génériques. |
| `git config --global core.excludesfile [file]` | Modèle d'ignorance à l'échelle du système pour tous les référentiels locaux |

### TEMPORARY COMMITS
_Stocker temporairement les fichiers modifiés et suivis afin de changer de branche_

| Commande | Description |
| ------- | ----------- |
| `git stash` | Enregistrer les modifications modifiées et mises en scène |
| `git stash list` | Liste des modifications de fichiers stockées dans l'ordre de la pile |
| `git stash pop` | Écrire en travaillant à partir du haut de la pile de réserve |
| `git stash drop` | Supprimer les modifications du haut de la pile de réserve |