###What kind of modified files did I stage in this Git repository?
>$ git diff --cached

this commands returns for example:

		$~/repos/developers-nootbook.github$ git diff --cached
		diff --git a/README.md b/README.md
		index e006b25..8caec22 100644
		--- a/README.md
		+++ b/README.md
		@@ -1,2 +1,2 @@
		 ### Move along, nothing to see here
		-[Questions?](http://lmgtfy.com/?q=Move+along%2C+nothing+to+see+here)
		+[Questions?](http://lmgtfy.com/?q=I+have+questions%2C+show+me+the+answers)
