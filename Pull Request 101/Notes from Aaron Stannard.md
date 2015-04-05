I'll try to illustrate the process for doing this by describing what I do.

First, you get your fork of Akka.NET - everything is cool.

Next, you clone it to your machine. Right now your "origin" is set to your local fork.
If Github for Windows doesn't do this for you automatically, you'll need to add a second remote to your local copy of your Akka.NET repository - one that points to the main repository (akkadotnet/akka.net)

git remote add upstream git@github.com:akkadotnet/akka.net.git

Now let's say you want to add a new feature - first thing you need to do is create a new feature branch. Don't work directly off of dev.

git create branch -b foo

Let's say it takes you a few days to get your work done. You make 5-6 commits along the way and push them to your feature branch (foo) on your local fork.

git push origin foo (keep a copy on Github, in case your machine dies)

During those few days, some other pull requests into the main Akka.NET repo were accepted. So before we can send in our PR we need to get those latest changes.

git checkout dev (go back to your local dev branch)
git fetch upstream
git merge --ff-only upstream/dev
git push origin dev (update your local fork's dev branch to be caught up with the central repo's)

Now your local dev branch is synced up with Akka.NET's dev branch.

Next, we need to go back to our foo branch and rebase on dev - that way all of our commits look like they came after those other changes that occurred on the dev branch.

git checkout foo

I STRONGLY RECOMMEND CREATING A NEW BRANCH HERE, because rebases literally rewrite your commit history. Bad things can happen.

git checkout -b foo-rebase

Next, let's rebase on dev.
git rebase dev

There might be some merge conflicts here - who knows? Work through those.

Cool, now you have all 5-6 of your commits stacked on stop of the latest changes on dev. We need to squash those 5 commits into a single commit next.

git rebase -i dev (interactive rebase - will pop up a text editor and ask you to pick / squash commits.)

Here's what the input of your squash should look like in the first text editor window

pick (oldest commit id)
squash (2nd oldest)
squash (3rd oldest)
squash (4th oldest)
squash (newest)

This will merge all of your previous commits into the first commit, which makes it really easy for others to review your work on the PR.

You'll also have to edit the commit message for these squashed commits - that part is pretty self-explanatory.

Next, once this is alllllllll done - we can send our PR.

git push origin foo-rebase

SEND IN PR HERE.

Rinse and repeat for multiple feature branches. No need to delete or refork, although it's a good idea to delete old feature branches from time to time. Notice that we never send a PR using the original foo branch? That's totally OK! We just use it for backup - the real PR only comes from the rebased branch.