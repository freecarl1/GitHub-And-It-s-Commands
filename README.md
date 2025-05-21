GitHub & It's Commands
============
*Git is the free and open source distributed version control system that's responsible for everything GitHub related that happens locally on your computer. This cheat sheet features the most important and commonly used Git commands for easy reference.*


## Translated Versions
- [Version Française](READMEfr.md)
- [Türkçe Versiyon](READMEtr.md)
- [Versión en Español](READMEes.md)


### INSTALLATION & GUIS
_With platform specific installers for Git, GitHub also provides the ease of staying up-to-date with the latest releases of the command line tool while providing a graphical user interface for day-to-day interaction, review, and repository synchronization._

#### GitHub for Windows
_https://windows.github.com_

#### GitHub for Mac
_https://mac.github.com_

_For Linux and Solaris platforms, the latest release is available on the official Git web site._

#### GitHub for All Platforms
_http://git-scm.com_

### SETUP
_Configuring user information used across all local repositories_

| Setup |
|-------|
|`git config --global user.name “[firstname lastname]”` <br/> Set a name that is identifiable for credit when review version history|
|`git config --global user.email “[valid-email]”` <br/> Set an email address that will be associated with each history marker|
|`git config --global color.ui auto` <br/> Set automatic command line coloring for Git for easy reviewing|

### SETUP & INIT
_Configuring user information, initializing and cloning repositories_

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize an existing directory as a Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Retrieve an entire repository from a hosted location via URL |

### STAGE & SNAPSHOT
_Working with snapshots and the Git staging area_

| Command | Description |
| ------- | ----------- |
| `git status` | Show modified files in working directory, staged for your next commit |
| `git add [file-name.txt]` | Add a file as it looks now to your next commit (stage) |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit your staged content as a new commit snapshot |
| `git reset [file]` | Unstage a file while retaining the changes in working directory |
| `git diff` | Diff of what is changed but not staged |
| `git diff --staged` | Diff of what is staged but not yet commited |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |
| `git remote -v` | View the remote repository of the currently working file or directory |

### BRANCH & MERGE
_Isolating work in branches, changing context, and integrating changes_

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | create a new branch at the current commit |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge the specified branch’s history into the current one |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |
| `git stash pop` | Apply latest stash to working directory |
| `git log` | Show all commits in the current branch’s history |

### Sharing & Updating Projects
_Retrieving updates from another repository and updating local repos_

| Command | Description |
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

| Command | Description |
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

| Command | Description |
| ------- | ----------- |
| `git rm [file]` | Delete the file from project and stage the removal for commit |
| `git mv [existing-path] [new-path]` | Change an existing file path and stage the move |
| `git log --stat -M` | Show all commit logs with indication of any paths that moved |

### REWRITE HISTORY
_Rewriting branches, updating commits and clearing history_

| Command | Description |
| ------- | ----------- |
| `git rebase [branch]` | Apply any commits of current branch ahead of specified one |
| `git reset --hard [commit]` | Clear staging area, rewrite working tree from specified commit |

### IGNORING PATTERNS
_Preventing unintentional staging or commiting of files_

| Command | Description |
| ------- | ----------- |
| `logs/`<br/>`*.notes`<br/>`pattern*/` | Save a file with desired paterns as .gitignore with either direct string matches or wildcard globs. |
| `git config --global core.excludesfile [file]` | System wide ignore patern for all local repositories |

### TEMPORARY COMMITS
_Temporarily store modified, tracked files in order to change branches_

| Command | Description |
| ------- | ----------- |
| `git stash` | Save modified and staged changes |
| `git stash list` | List stack-order of stashed file changes |
| `git stash pop` | Write working from top of stash stack |
| `git stash drop` | Discard the changes from top of stash stack |