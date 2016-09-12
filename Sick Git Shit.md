------------------------------------------------
Sick Git Shit
------------------------------------------------
.gitignore
gitignore.io (to generate for you)

*.DS_Store (generated when you change stuff in Finder, 
            i.e. arrange by, etc.)
*.iml (IDE module file)
.idea* (IDE(A) files) (IntelliJ IDEA)

------------------------------------------------
Removes file(s) from git tracking
------------------------------------------------
git rm --cached .DS_Store
git rm -r --cached .idea (recursive)

Deletes all .DS_Store files already tracked in git repo
find . -name .DS_Store -print0 | xargs -0 git rm -f --ignore-unmatch

------------------------------------------------
Shows all files tracked in git repo (vs ls -al)
------------------------------------------------
git ls-tree --full-tree -r HEAD

------------------------------------------------
Other commands
------------------------------------------------
git stash - save changes for later
git stash pop - abandon changes

git log - shows commit history

------------------------------------------------
Bash Alias for all these priceless gems
------------------------------------------------
cd - (go home)
vim .bash_profile

alias alias_name="command_to_run"

alias killjunk="find . -name .DS_Store -print0 | 
                xargs -0 git rm -f --ignore-unmatch"

source ~/.bash_profile (to load)

------------------------------------------------
Delete repository when the feds come knockin.
------------------------------------------------
rm -rf .git

------------------------------------------------
Refresher on git setup
------------------------------------------------
git status
git init
git add .
git commit - m ""
git remote add origin linkToRepo
git push -u origin master

The key is "argument-less git-pull". When you do a git pull from a
 branch, without specifying a source remote or branch, git looks at the
  branch.<name>.merge setting to know where to pull from. git push -u 
  sets this information for the branch you're pushing.

-- From fork
git clone link path
git remote -v (view remotes)
git remote add upstream linkToRepo
git remote -v (view remotes) (try again to see the difference)



