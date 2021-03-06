[notes](index.md) | [backend](backend.md) | [linux terminal](linux/terminal.md) | [tools](tools.md)

## git / GitHub
- [basics](#basics)
- [checkout](#git-checkout)
- [branch](#git-branch)
- [log](#git-log)
- [remote](#git-remote)
- [stash](#stash)
- [undoing](#undoing)
- [caching](#caching)
- [other](#other)
- [links](#links)

### basics
`git init` initialize project as git repo

`git clone https://github.com/dev-academy-programme/karearea-2016.git` - clone git repository to local machine

`git add .` / `git add -A` / `git add filename` - stage files to be committed

`git status` - see status of repository

`git commit -m "message about commit"` - commit staged files/changes to repository

`git push` - push files to github repository

`git pull` - pulls down changes from remote repository (pull = fetch + merge)

`git pull -r` - pulls down changes and rebases them to be before commits on local branch

### git checkout
- `git checkout branchName` - switch to newBranchName
- `git checkout -b newBranchName` - create & checkout new branch

### git branch
- `git branch --all` - displays all branches, verbose
- `git branch new_branch_name` - create new branch in local repository
- `git branch -d <branch name>` - delete a branch

### git log
- `git log` - lists all the commits
- `git log --since='2013-06-09` - since specified date
- `git log since ='2 weeks ago'` - since 2 weeks ago
- `git show sha-key`


### git remote
- `git remote -v` - displays all remotes, verbose
- `git remote add origin` https://github.com/jess-of-the-woods/react-the_first.git - adds origin
- `git remote rm origin` - removes remotes
- `git remote prune origin` - deletes local cached version of branches that have been deleted on github

## stash
- `git stash save 'here is a message describing what I just did'` or `git stash`: Stash changes
- `git stash list`: Lists all stashes
- `git stash apply stash@{0}`: Applies `stash@{0}` but doesn't clear the stash, i.e. it remains there to be used
- `git stash pop`: Applies most recent stash, drops it from stash
- `git stash drop stash@{0}`: Drops specified stash
- `git stash clear`: Drops all stashes


## undoing
<img src='https://i.stack.imgur.com/caci5.png'>

3 trees ( collections of files ):  Working directory, Index, HEAD

[difference between HEAD / Working Tree / Index in Git](https://stackoverflow.com/questions/3689838/difference-between-head-working-tree-index-in-git)

If you commit node modules on 1st commit..
- `rm -rf .git`
- `git init`

### reset
Move the branch HEAD points to (stop here if --soft)

Make the Index look like HEAD (stop here unless --hard)

Make the Working Directory look like the Index

`git checkout e8723hdk79`: checkout previous commit

`git reset index.html`: un add staged files

`git reset --soft HEAD ~1`: uncommit changes, x number of commits


If all you want to do is undo the act of committing, leaving everything else intact, use: `git reset --soft HEAD^`

If you want to undo the act of committing and everything you'd staged, but leave the work tree (your files intact): `git reset HEAD^`

And if you actually want to completely undo it, throwing away all uncommitted changes, resetting everything to the previous commit (as the original question asked): `git reset --hard HEAD^`


### revert
`git revert commitId` ( does an anti-commit, undo commit, but is still available )

## caching
- `git config user.name`: display user name
- `git config user.email`: display user email
- `git config --list`: list all config details
- `git config --global credential.helper cache` - cache password in git
- `git config --global credential.helper 'cache --timeout=3600'` - timeout = 1 hour

## other
`git merge --abort`

`git remote add upstream git-repo-url`

`git fetch upstream`

`git pull upstream master`

`git merge upstream master`

origin is fork
upstream is where fork comes from

1. `git pull upstream master`
2. `git checkout -b awesome-changes`
3. Make some changes
4. `git status`, `git add .` commit
5. `git push -u origin awesome-changes` ( -u = set upstream )
6. Compare & pull request

see the size of a github repo before cloning it?
`curl -I https://codeload.github.com/ManojkumarMuralidharan/Excite-Bike3D/zip/master`

---

### links
- [creating-project-pages-manually](https://help.github.com/articles/creating-project-pages-manually/)
- [Dan Gitschooldue](https://www.youtube.com/channel/UCshmCws1MijkZLMkPmOmzbQ) - YouTube channel

#### stash
- [Stashing & Cleaning](https://git-scm.com/book/en/v2/Git-Tools-Stashing-and-Cleaning)
- [Git Tutorial: Using the Stash Command](https://www.youtube.com/watch?v=KLEDKgMmbBI) - YouTube (10 mins)
