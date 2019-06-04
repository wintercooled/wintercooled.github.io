
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

## If we have two branches to merge into master on the server

This is the same as clicking merge on GitLabs, GitHub etc but here we need to merge one branch, then another then push.

Check we're in sync with master:

git checkout master

git status

Should tell you you are in sync with origin/master

Now merge in one of the branches:

git merge --ff-only branch-one

Should fast-forward and tell you what changes were applied

Check with:

git status

Will show you how many commits ahead you are (the commits made to branch-one)

Now to merge the other branch (branch-two) in.

Checkout the second branch and rebase to local master by following steps below:

git checkout branch-two

git log

(press q to quit log if it is long enough to start paging)

You will see that the 'HEAD ->' of the branch is on top of (origin/master, origin/HEAD) (the last update to the origin copy of master) as it doesn't have the commits under it that were added to branch-one. So you should see commits for branch-two above origin/master, origin/HEAD. We need to rebase master into it so our branch-two commits are on top of the commits from branch-one that we made to master (local).

This means we need to rebase or trying to merge will result in detached HEAD. So we will rebase master into branch-two.

git rebase master 

git log

You will now see the commits for branch-one between (origin/master, origin/HEAD) and the commits for branch-two. The commits for branch-one will show as (origin/branch-one, master, branch-one), which is on top of (origin/master, origin/HEAD). So we have rebased master (with its branch-one commits made on top of origin/master into branch-two.

So now we need to merge branch-two into master (local):

git checkout master

git merge --ff-only branch-two

git log

We should see that HEAD -> is now on master (HEAD -> master, branch-two) and that the other commits for branch-one are under it.

Now we can push to origin master:

git push
(or git push origin master)

# References

Rebase v Merge: https://hackernoon.com/git-merge-vs-rebase-whats-the-diff-76413c117333

tl;dr: The one-line summary: don’t rebase a branch unless you are the only one who uses it.

Use merge in cases where you want a set of commits to be clearly grouped together in history

Use rebase when you want to keep a linear commit history

DON’T use rebase on a public/shared branch
