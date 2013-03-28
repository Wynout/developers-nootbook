###What kind of modified files did I staged in this Git repository?
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


### Tried to push, but remote already has changes

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

### Don't want to commit changes now, but change branch? - Git Stash
Stash the changes
[http://git-scm.com/book/en/Git-Tools-Stashing](http://git-scm.com/book/en/Git-Tools-Stashing)

>$ git stash

To see the list of stashes you stored:
>$ git stash list

	stash@{0}: WIP on master: 3a512ee Add link setting up sublime text for PHP dev
	stash@{1}: WIP on master: 1418cbe Fixed type, again... Think McFly Think!.
	stash@{2}: WIP on master: af3e481 Removed Youtube link

To apply the last stashed changes
>$ git stash apply

To apply change from #2 in stash list:
>$ git stash apply stash@{2}

To remove the change from the stash list #2:
>$ git stash drop stash@{2}

To apply the stash and immediately drop it from your stack:
>$ git stash pop
