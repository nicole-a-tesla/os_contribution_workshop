# Example git workflow

*Note*: this is one common workflow, but there are variations. Check your project's docs for details on how it uses git.

* **Fork original repo**
	* Make a copy of the code base that lives on your GitHub account. [[docs](https://help.github.com/articles/fork-a-repo/)]
* **Clone your new fork onto your computer**
	* Copy the code on GitHub onto your computer [[docs](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository#Cloning-an-Existing-Repository)]
	* `git clone <CLONE LINK TO YOUR FORK>`
* **Set the upstream to the original repository**
	* Tell the code on your computer about the original code base. This allows you to pull in any changes that are made to the original project while you are working on your contribution [[docs, see steps 6-8](https://help.github.com/articles/fork-a-repo/#step-3-configure-git-to-sync-your-fork-with-the-original-spoon-knife-repository)]
	* `git remote add upstream <CLONE LINK TO ORIGINAL REPO>
* **Create feature branch**
	* Make a workspace devoted to this feature
	* `git checkout -b <FEATURE NAME>`
* **Make your contribution!**
* **Pull upstream master into your local master**
	* Get any changes to the original codebase sine you started working. [[docs](https://help.github.com/articles/syncing-a-fork/)]
	* `git checkout master` and then `git pull upstream master`
* **Rebase feature branch on your master**
	* Change the history of your feature branch to include the changes you pulled in from the upstream repo [[docs](https://git-scm.com/book/en/v2/Git-Branching-Rebasing)]
	* `git checkout <FEATURE BRANCH>` and then `git rebase master`
* **Resolve any merge conflicts**
	* Resolve any conflicts between your work and the new version of the original repo. If there are none, yay! Skip this step [[docs](https://help.github.com/articles/resolving-a-merge-conflict-from-the-command-line/)]
* **Push your changes to `origin <BRANCHNAME>`**
	* Send your feature branch to GitHub [[docs](https://help.github.com/articles/pushing-to-a-remote/)]
	* `git push origin <FEATURE BRANCH>`
* **Open pull request**
	* Ask the repo owner to merge your changes into the codebase. The base of your PR should be the master branch of the original repository. The "compare" branch should be the feature branch of your fork. [[docs](https://help.github.com/articles/about-pull-requests/)]
* **Wait for project owners to review your changes. Alter PR as requested.**