# Git
  - tryGit = 09:30 tot 10:00 15/30+- setup md file
  - Git Real = 10:00 tot 13:30 3.5 uur met eten
  - Git Real2 = 13:30 tot 14:55 zo: 18:30 tot 19:37

## Cource cheatsheed

  | Git commands                 | Function
  | :--------------------------- | :--------
  | **Try Git** ||
  | `git init` | Make project
  | `git status` | Status
  | `git add test.txt` | Add file to git
  | `git add '\*.txt'`| Multipel add file to git
  | `git add --all`| all files
  | `git commit -m "Add test.txt"` | Commit changes
  | `git log` | Views commits
  | `git remote add origin https://github.com/try-git/try_git.git` | Add new em[ty GitHub origin is the name of the remote
  | `git push -u origin master` | -u is for remember parameters
  | `git push` | push to server
  | `git pull orgin master` | pull to server
  | `git diff` | shows changes
  | `git diff HEAD` | diff with last changes
  | `git diff --staged` |
  | `git reset` | removed unstage files
  | `git checkout -- text.txt` | removed all changes since last commit for text.txt
  | `git branch clean_up` | make branch
  | `git checkout clean_up` | switch to branch
  | `git branch` | views branch
  | `git rm '\*.txt'`| remove files and staged
  | `git rm -r folder_test` | remove folder and staged
  | `git merg clean_up` | merg branch to master
  | `git branch -d clean_up` | removed branch
  |||
  | **Git Real** ||
  | `git reset --soft HEAD^` | revert last commit and put changes into staging
  | `git commit --amend -m "New Message"` | add files to last commit
  | `git reset --hard HEAD` | undo last commit and all changes
  | `git reset --hard HEAD^` | undo last one parent commit and all changes
  | `git reset --hard HEAD^^` | last to commit and all changes
  | `git commit -a -m "New Message"` | stage and commit all
  | | |
  | `git checkout -- text.html text2.html` | checkout Multipel files
  | | |
  | `git checkout -b branchname` | make branch and checkout (set branch as working)
  | | |
  | `git merge branchname` | merg in curent branch
  | `git commit -a` | after a merge conflict is fixed
  | | |
  | `git branch -r` | view remote branch
  | `git remote show origin` | view remote branch
  | `git push origin :branchname` | deletes remote branch
  | `git branch -d branchname` | deletes local branch (error if changes open)
  | `git branch -D branchname` | deletes local branch (always)
  | `git remote prune origin` | clean up remote branches
  | | |
  | `git push heroku-staging staging:master` | push local staging to master herocu link thing
  | | |
  | `git tag` | list tags
  | `git checkout tagname` | checkout code at commit
  | `git tag -a tagname -m "tage message"` | add new tag
  | `git push --tags` | push new tags
  | | |
  | `git push origin branchname` | push branch to remote
  | | |
  | `git rebase --skip` | skip this patch instead run
  | `git rebase --abort` | stop rebasing and checkout original branch
  | ``git fetch`` | get changes from master
  | | |
  | ``git diff HEAD^`` | parent of latest commit
  | ``git diff HEAD~5`` | five commits ago
  | ``git diff HEAD^..HEAD`` | second most recent commit vs most recent
  | ``git diff branchname anothere branchname`` | compare 2 branches
  | ``git blame index.html`` | shows how dit it
  | ``git rm --cached file.txt`` | remove file from git but not filesystem
  | | |
  | `git log --pretty=oneline` | log on one line
  | `git log -p` | log with diff (changes)
  | `git config --global user.name "Leroy"` | for al repos
  | `git config user.name "Leroy"` | for curent repos
  |||
  | `git config --global alias.co checkout` | set check
  |||
  | **Git Real 2** ||
  | `git rebase master` ||
  | `git rebase -i HEAD~4` | for interactive rebase|
  | reword .... | after you get real change for the name|
  |||
  | NoteStash | commat all or rollback  |
  | `git stash save "mesage"` | save stash |
  | `git stash save --keep-index` | for only unstaged files |
  | `git stash save --include-untracked` | for only untrecked files |
  | `git stash apply` | apply stage (git diff) (top stash (stash@{0}))|
  | `git stash list` | list |
  | `git stash list --stat` | list more info |
  | `git stash show stash@{0}` | more info |
  | `git stash show stash@{0} --patch` | more info with code |
  | `git stash apply stash@{1}` | by name|
  | `git stash drop` | remove a stash (top stash (stash@{0})) |
  | `git stash pop ` | apply drop |
  | `git stash branch branchname ` | stash on branch |
  | `git stash clear` | remove all |
  | `git clone reponame newreponame` | backup |
  |||
  | `git filter-branch --tree-filter 'rm -f passwords.txt'` | remove passwords.txt fro githistory ('find . -name "\*.mp4" -exec rm {} \;') -f in command is for no fail if file don't exsit. |
  | `git filter-branch -f --prune-empty --tree-filter ..` | the -f after branchname is for force so it overwrite backup --prune-empty removes empty commits |
  | `git filter-branch --tree-filter 'command' -- --all` | trow all files |
  | `git filter-branch --tree-filter 'command' -- HEAD` | trow all files |
  | `git filter-branch --index-filter 'git rm --cached --ignore-unmatch passwords.txt'`| trow all commits |
  |||
  | `git config --global core.autocrlf input` | linux format text |
  | `git config --global core.autocrlf true` | windows format text |
  |||
  | .gitattributes | \* text=auto \*.bat text eol=crlf \*.sh text eol=lf \*.png binary \*.js text|
  |||
  | `git cherry-pick 5321` | pick a commit and aplly to current branch |
  | `git cherry-pick --edit 5321` | with comment |
  | `git cherry-pick --no-commit 5684 5321` | 2 commits same time  |
  | `git cherry-pick -x 5684` | adds source commit message |
  | `git cherry-pick --signoff 5684` | adds current user to commit |
  |||
  | `git submodule add git@example.com:css.git` | add submodule after commit and push |
  | .gitmodules | path and url |
  | `git submodule init` | init submodule from .gitmodules |
  | `git submodule update` | get the modules and update |
  | submodule change | git add git commit (need to be in branch) git push if no branch then git merge 6464  push summodule and parrent|
  | `git push --recurse-submodules=check` | check if submodules are push |
  | `git push --recurse-submodules=on-demand` | push parent and submodules |
  | `git config alias.pushall "push --recurse-submodules=on-demand"` | config for push all |
  |||
  | `git branch temp_changes a7eded4` | make branch out of commit  |
  |||
  | `git reglog` | seconde log backup log (local) |
  | `git reset --hard 1e62` | to get from the reglog (or 1e62 can also be HEAD@{1}) |
  | `git log --walk-reflogs` | more info |
  | | |
  | **Mastering GitHub** | 20:30  met git install tot 22:00 |
  | `git config --system color.ui true` | --local --global --system change the color  |
  | `git config --global --list` | view all configs email name .. (.gitconfig) |
  | `git config --local --list` | view all configs email name .. (.git/config) |
  | `git config --global core.autocrlf input` | linux format text |
  | `git config --global core.autocrlf true` | windows format text |
  | `git config --global push.default simple` | push one branch insted of all  |
  | `git pull --rebase` | better than git pull |
  | `git config --global pull.rebase true` | better than git pull set to default |
  | `git config --global rerere.enabled true` | if merge alread than makes it the same |
  | `git status -s` | compact version of status |
  | `git config --global alias.s "status s"` | NICE alias for status s |
  | `git config --global alias.lg "log --oneline --decorate --all --graph"` | NICE alias for log |
  | repo for .config |  |
  | `git commit -am -m "New Message"` | add and commit
  | `git remote add upstream repoPath` |  |
  |  |  |
  | `git merge --no-ff branchname` | no fast-forward merge |
  | |  |
  | `git tag` | lightweight |
  | `git tag -s` | signed |
  | `git tag -a` | annotated (most case) |
  | semver.org | more over tags |
  | |  |
  | `git branch -d release_branch_1.0` | remove local |
  | `git push origin --delete release_branch_1.0` | remove remote |



## rebase
  - git checkout branchname
  - git fetch
  - git rebase master
  - git checkout master
  - git merge admin
  - CONFLIST
  - resolve
    - git add file.txt
  - git rebase --continue

## rebase split the file
  - git rebase -i HEAD~4
  - set pick to edit in file
  - git reset --soft HEAD^
  - recommitted changes so add file 1 add file 2
  - git rebase -- continue

## rebase files combine
  - git rebase -i HEAD~4
  - set edit in file last commit down
  - set comment

## update fork after pull request
    - git remote add upstream pathToRepo
    - git fetch upstream
    - git merge upstream/master master
    - git push origin master
    - git pull upstream master

    - git fetch
    - git branch -a (list branches)
    - git checkout branchNAAM
    -
