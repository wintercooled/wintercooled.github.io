
## Branching (untested)

Get latest from origin or upstream (below is based off working on clone, not fork)

git checkout master

git fetch origin

git rebase

Create branch off of that code:

git branch my-branch

git checkout my-branch

Changes to files...

Commit changes to remote my-branch:

git add --all

git commit -m "message"

If other changes then get merged into master before my-branch gets merged....

Get those changes into master:

git checkout master

git fetch origin

git rebase

Merge those changes into my-branch:

git checkout my-branch

git rebase master

Push that merge to the remote branch:

git push

## Working on someone else's branch

git pull --all

git checkout --track origin/branch-name-here

--track is shorthand for git checkout -b [branch] [remotename]/[branch]

then just edit, add and commit as normal
