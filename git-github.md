#Git / GitHub

##Undoing
3 trees ( collections of files ):  Working directory, Index, HEAD

If you commit node modules on 1st commit..
  `rm -rf .git`
  `git init`

###Reset:
  Move the branch HEAD points to (stop here if --soft)
  Make the Index look like HEAD (stop here unless --hard)
  Make the Working Directory look like the Index

  `git checkout e8723hdk79` ( checkout previous commit )

  `git reset index.html` ( un add staged files )
  `git reset --soft HEAD ~1` ( uncommit changes, number of commits )

###Revert
  `git revert commitId` ( does an anti-commit, undo commit, but is still available )

---

###Git remote
`git init` initialize project as git repo

`git remote -v` - displays all remotes, verbose

`git remote add origin` https://github.com/jess-of-the-woods/react-the_first.git - adds origin

`git remote rm origin` - removes remotes

`git remote prune origin` - deletes local cached version of branches that have been deleted on github


`git help commit` - ?



`git clone https://github.com/dev-academy-programme/karearea-2016.git` - clone git repo to local machine

`git checkout branchName` - switch to newBranchName

`git checkout -b newBranchName` - create & checkout new branch

`git add .` / `git add -A` / `git add filename` - stage files to be committed


`git status` - see status of repository

`git commit -m "message about commit"` - commit staged files/changes to repository

`git push` - push files to github repository

### Git Branch
- `git branch --all` - displays all branches, verbose
- `git branch new_branch_name` - create new branch in local repository
- `git branch -d <branch name>` - delete a branch

### Git log
- `git log` - lists all the commits
- `git log --since='2013-06-09` - since specified date
- `git log since ='2 weeks ago'` - since 2 weeks ago

  `git show sha-key`


`git pull` - pulls down changes from remote repository (pull = fetch + merge)
`git pull -r` - pulls down changes and rebases them to be before commits on local branch

[creating-project-pages-manually](https://help.github.com/articles/creating-project-pages-manually/)

---

`git merge --abort`

`git remote add upstream git-repo-url `
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

---

See the size of a github repo before cloning it?
`curl -I https://codeload.github.com/ManojkumarMuralidharan/Excite-Bike3D/zip/master`
---

###Password Caching
`git config --global credential.helper cache` - cache password in git

`git config --global credential.helper 'cache --timeout=3600'` - timeout = 1 hour
