# LearnEnoughGit2.0-with-Laiza-Arriesgado
## Laiza Arriesgado - 2025

## Overview
This repository contains the assignment, code and resources from the "Learn Enough Git to Be Dangerous" textbook.
Here, you will find the code snippets and exercises that is part of the book, along with additional resources to help the writer and readers understand Git and GitHub as version control better.

## Installation & Set-Up
1. Download and install Git from the official website: [Git Downloads](https://git-scm.com/downloads). Follow the instructions for your operating system.
2. Ensure that you have a sufficient version of Git installed. You can check your Git version with:
   ```bash
   git --version # should be at least 2.28.0 
   ```
3. Clone or download this repository to your local machine:
   ```bash
   git clone <repository-url>

## The Assignment - The Making
1. Exercise 3.1.1
    -Verified that `git push` successfully pushes, adding a new image to the repository.
    - `git log -p` command was used to view the commit history and changes made with a less interface.
    - Using the `git log --oneline, the commit that added the HTML DOCTYPE was identified. The SHA of the commit was `931cde4`
2. Exercise 3.2.1
    -`.gitignore` file was created and committed. Running `git commit -am` is not enough to add the file, as it is not tracked by Git. The command `git add .gitignore` was used to stage the file before committing.
    -`git push` was used to push the changes to the remote repository.
3. Exercise 3.3.2
    - Deleted branch about-page (was ff3c56a).Confirmed by running `git branch` that only the `main` branch is left.
    - `test-branch` was created by running `git branch test-branch` 
    - `test-branch` is checked out by running `git checkout test-branch` and using the touch command to create `test.txt` file. Running `git add -A` to add the file, checked out using `git checkout test.txt` and committing by running `git commit -m "Add test.txt file"
    - Switched to branch `main` by running `git checkout main` and tried deleting the test-branch using `git branch -d` and confirmed that it doesn't work. Successfully deleted test-branch by running `git branch -D test-branch`
    - 
4. Exercise 3.4.1
    - Created a file called `rid.txt`, adding it by running `git add -A` and deleting using `git checkout -f`
    - Tried running the "long form" option `git checkout --force` and the result is the same as "short form" (`git checkout -f`) option.
5. Exercise 4.1.1 (I made another account to see what it would look like in real time when having collaborators)
    - Run `git log` and double-check the details using `git log -p`
    - Attribution under the Creative Commons Attribution-NoDerives 2.0 Generic license was added, committed, and pushed to GitHub.
    - Using the newly created GitHub as a collaborator, I ran `git pull` and verified the changes made by refreshing the browser and by running `git log -p`
6. Exercise 4.2.3
    - Changed the default Git editor from Vim to Atom.
	```
	git config --global core.editor "atom --wait" 	# `--wait` tells Git to pause and wait until you close the file in Atom
	git commit					                    # Git checks for changes to commit
	git config --global core.editor			        # Confirm editor setting - should return `atom --wait`
	```
    - Adding the required attribution under the Creative Commons Attribution 2.0 Generic license. Running `git commit -a` without `-m` and a command line message. Quitting the editor without including a message cancels the commit.
    - Run `git commit -a` and added the commit message "Add polar bear attribution link". Adding a longer message after hitting return a couple of times.
    - Run `git log` confirming that both short and longer messages appear correctly, and `git push` the changes after.
    - Using the collaborator account, I run `git pull` to the About page. Verified by refreshing and running `git log -p`, confirming that the repository has been properly updated. 
7. Exercise 4.3.1
    - Using the collaborator account, running `git pull` to update the merge committed, and is confirmed using `git log`
    - Deleted the `fix-trademark` branch locally
	```
	`git checkout main`		        # switch to `main` branch or use of `git branch --show-current` to confirm current branch
	`git branch -d fix-trademark`	# -d is sufficient because it has been merged and a safe option
					                # -D is forcing you to delete a branch if it hasn't been merged yet.

## Additional Resources and References
1. Hartl, M. (n.d.). "Learn Enough Git to Be Dangerous". Retrieved from https://www.learnenough.com/git-tutorial
2. Creative Commons Attribution 2.0 Generic License. Retrieved from https://creativecommons.org/licenses/by/2.0
