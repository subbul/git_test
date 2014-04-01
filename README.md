Git
References:

http://gitref.org/index.html


mkdir git_training

git init

vi README.md

git status ( suggests git add)

git add .

git status ( newfile: readme.md - staged)

git commit -m "First version"

git log

vi README.md (modify by adding one more line)

git diff ( shows the new line as + with commited or Staged)

git add .

(DO NOT COMMIT YET)
vi README.md (add third line)

git diff ( shows only third line- as it compares with NOT staged working file OR NOT commited file with last commited)
git diff --cached ( shows diff between STAGED and last comitted)

git diff HEAD ( shows the diff between committed and working copy and staged)

git commit -a -m "Added two more lines"

git remote -v ( lists all remore repository)

Now go to GIT_Hub ( crate a new repository online)

get the HTTPS or SSH ( https://github.com/subbul/git_test.git, git@github.com:subbul/git_test.git)

git remote add  origin git@github.com:subbul/git_test.git

[Check SSH setting in git hub settings for adding any keys]
git push origin master ( pushing to Origin(thats remote) the master branch which is default created branch)


Check in Github online. you should be seeing REAME.md pushed

vi README.md (add a line from PC)

git commit -a -m "changs in PC"

DIFF WITH LOCAL with REMOTE ( git diff ..origin/master)

git push -u origin master (push master branch to origin for new changes in local)

Edit README.md in GIT HUB online and save (commit there)

git diff ..origin/master (nothing gets reflected)

git fetch origin master ( get the latest update from remote, not MERGE or update local.. just available for diff etc)

git diff FETCH_HEAD ( shows the changes from remote)

git pull origin master ( fetches and merges)

Fetch is to update local and to know what changes and what needs to be taken in(no merge, your local rep history will reflect the changes, but doesn't get the change)
merge then to apply change


git log --oneline --all --graph -decorate (shows branch data and the head)

gitk (GUI shows the commits diffs)
gitk -all (all branches)


Create a newfile.txt in GITHUB onilne

git diff FETCH_HEAD ( shows newfile.txt)


git branch ( list all branches)
git checkout -b feature_1 ( create a new branch "feature_1" and switch to that, it contains all the files or master branch)

vi newfile.txt ( Edit to say "Modifying in branch")

git commit -a -m "Modifying file in PC branch"

git branch ( shows * on the active branch)

git push origin feature_1 ( Push the feature_1 branch to remote server)

Go to Git Hub and check for "feature_1" branch and the newfile.txt modified reflecting

Go back to PC

git checkout master

git diff feature_1 newfile.txt ( shows the diff between newfile.txt in "master" and "feature_1" branch)

git merge feature_1 ( takes the changes from feature_1 to current branch - "master")


if a branch, has occured after pt A in master , commits B& C are done in master
commits B1 & C1 are done in branch.
Rebase will rewind B &C, apply B1 & C1 and then B & C
rebase ( pull the individual commits from branch and reapply other commits on main branch)
Rebase is different from merge as it holds individual commits, rather a single commit alone.
git push origin master


vi newfile.txt ( add "going to modify or put in stash")re

git stash ( current changes to stash a temporary storage and working directory or copy is reverted to cleanslate)

git stash list ( lists all the stashed items)

git stash apply ( resume the copy which was stashed recently..)
git stash pop ( will do apply and remove the item from stash)


git pages (subbul.github.io, subbul.github.io/project)
git add -i (prompts for interactive add)
