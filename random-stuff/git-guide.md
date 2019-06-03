
## Branching

Get latest from origin or upstream (below is based off working on clone, not fork)

git checkout master

git fetch origin

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

Merge those changes into my-branch:

git checkout my-branch

git rebase master

Push that merge to the remote branch:

git push
