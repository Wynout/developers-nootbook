# Git common commands

## Git diff --cached
**What kind of modified files did I stage in this Git repository?**

>$ git diff --cached

This commands returns for example:

		$~/repos/developers-nootbook.github$ git diff --cached
		diff --git a/README.md b/README.md
		index e006b25..8caec22 100644
		--- a/README.md
		+++ b/README.md
		@@ -1,2 +1,2 @@
		 ### Move along, nothing to see here
		-[Questions?](http://lmgtfy.com/?q=Move+along%2C+nothing+to+see+here)
		+[Questions?](http://lmgtfy.com/?q=I+have+questions%2C+show+me+the+answers)


-------------------------------

## Git push - non-fast-forward updates were rejected
**Tried to push, but remote already has changes**

>$ git push

		To git@github.com:Wynout/developers-nootbook.git
		 ! [rejected]        master -> master (non-fast-forward)
		error: failed to push some refs to 'git@github.com:Wynout/developers-nootbook.git'
		To prevent you from losing history, non-fast-forward updates were rejected
		Merge the remote changes (e.g. 'git pull') before pushing again.  See the
		'Note about fast-forwards' section of 'git push --help' for details.\

First we need to merge te remote changes in our repository:

>$ git pull

		remote: Counting objects: 11, done.
		remote: Compressing objects: 100% (7/7), done.
		remote: Total 9 (delta 5), reused 6 (delta 2)
		Unpacking objects: 100% (9/9), done.
		From github.com:Wynout/developers-nootbook
		   4442be4..c95acfa  master     -> origin/master
		First, rewinding head to replay your work on top of it...
		Applying: Create TODO file

Now we can push our changes to the remote origin:

>$ git push

		Counting objects: 4, done.
		Delta compression using up to 4 threads.
		Compressing objects: 100% (2/2), done.
		Writing objects: 100% (3/3), 312 bytes, done.
		Total 3 (delta 1), reused 0 (delta 0)
		To git@github.com:Wynout/developers-nootbook.git
		   c95acfa..9382888  master -> master

Mission accomplished. Done.

-------------------------------

## Git Stash
**Don't want to commit half-done work, but change branch?**

[http://git-scm.com/book/en/Git-Tools-Stashing](http://git-scm.com/book/en/Git-Tools-Stashing)

Often, when you’ve been working on part of your project, things are in a messy state and you want to switch branches for a bit to work on something else. The problem is, you don’t want to do a commit of half-done work just so you can get back to this point later. The answer to this issue is the git stash command.

>$ git stash

To see the list of stashed changes you stored:
>$ git stash list

	stash@{0}: WIP on master: 3a512ee Add link setting up sublime text for PHP dev
	stash@{1}: WIP on master: 1418cbe Fixed typo, again... Think McFly Think!.
	stash@{2}: WIP on master: af3e481 Removed Youtube link

To apply the last stashed changes
>$ git stash apply

To apply change from #2 in stash list:
>$ git stash apply stash@{2}

To remove the change from the stash list #2:
>$ git stash drop stash@{2}

To apply the stash and immediately drop it from your stack:
>$ git stash pop

-------------------------------

## Cloning

[source](https://help.github.com/articles/fork-a-repo)

>$ git clone https://github.com/username/Spoon-Knife.git

To keep track of the original repository, you need to add another remote named *upstream*

>$ git remote add upstream https://github.com/username/Spoon-Knife.git

		From https://github.com/username/Spoon-Knife
		 * [new branch]      master     -> upstream/master

Fetch any new changes in from the original repository, without modifying your files

>$ git fetch upstream

Merge any changes fetched into your working files

>$ git merge upstream/master

-------------------------------

## Undo a commit and redo

[source](http://stackoverflow.com/questions/927358/how-to-undo-the-last-git-commit)

>$ git reset --soft HEAD^
>$ git commit -c ORIG_HEAD

-------------------------------