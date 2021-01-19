# bikesharesystem
## team project

### GIT WORK FLOW
#### Before start
	make sure you have added your own ssh-key to your github account.
---
#### Start to synchronize and develop
	1. Fork another repo on github to your own github account.
	2. Clone this forked repo from your own github account. (git clone)
	3. Now you can see there is only a master branch on your local repo and you are on the master branch.
	4. `git remote -v` to check origin repo if you have `upstream` configured.
			if not do so, you will see:
			```
				origin  info of your own origin repo (fetch)
				origin  info of your own origin repo (push)
			```
			if do so:
			```
				upstream  info of your own upstream repo (fetch)
				upstream  info of your own upstream repo (push)
			```
	5. `git remote add upstream https://github.com/HiChen85/bikesharesystem.git` to add upstream.
	6. `git remote -v ` to check again.
	7. when you done above processes, then you need to create a local dev branch because you only have master on your local repo.
			`git switch -c dev origin/dev` this will switch to and connect the local branch and origin branch.
	8. `git fetch upstream` this will synchronize your remote repo and upstream repo but not merged.
	9. when you have fetched, you must to merge upstream updates to your local repo.
			`git merge upstream/dev` because we don't want the master branch to be changed frequently, so I suggest to merge upstream/dev branch to your local dev branch.
	10. Then, you have updated your local repo but haven't pushed to your remote(origin) repo. So you aslo need to do this process.
			`git push origin dev` make sure your push this updates to your own remote(origin) dev branch not master.
	11. Afterwards, you can start your development, add, commit, push your changes to this forked repo.
	11. Finally, create a new pull request to upstream repo owner on github.
		
