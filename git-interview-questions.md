## Git Interview Questions
### Easy Questions:
1. What is Git?

 - Git is a distributed version control system designed to handle everything from small to very large projects with speed and efficiency. It allows multiple developers to work on the same project without interfering with each other.

2. How do you initialize a new Git repository?

 - You can initialize a new Git repository using the command:
 > git init

3. How do you clone a repository?

 - You can clone a repository using the command:
 > git clone <repository-url>

4. How do you check the status of your repository?

 - You can check the status of your repository using the command:
 > git status

5. How do you stage changes for a commit?

 - You can stage changes for a commit using the command:
 > git add <file-or-directory>

6. To stage all changes, you can use:
 > git add .

7. How do you commit staged changes?

 - You can commit staged changes using the command:
 > git commit -m "commit message"

8. How do you view the commit history?

 - You can view the commit history using the command:
 > git log

9. How do you create a new branch?

 - You can create a new branch using the command:
 > git branch <branch-name>

10. How do you switch to a different branch?

 - You can switch to a different branch using the command:
 > git checkout <branch-name>
How do you merge a branch into the current branch?

 - You can merge a branch into the current branch using the command:
 > git merge <branch-name>

## Moderate Questions:
1. How do you delete a branch?

 - You can delete a branch using the command:
 > git branch -d <branch-name>

To force delete a branch, you can use:
 > git branch -D <branch-name>

2. What is the difference between git fetch and git pull?

 - git fetch downloads changes from the remote repository but does not apply them to your working directory.
 - git pull downloads changes from the remote repository and applies them to your working directory (essentially a combination of git fetch and git merge).

3. How do you resolve a merge conflict?

 - To resolve a merge conflict, you need to manually edit the conflicting files to fix the conflicts, then stage the resolved files using git add, and finally commit the changes using git commit.

4. How do you create a new branch and switch to it?

 - You can create a new branch and switch to it using the command:
 > git checkout -b <branch-name>

5. How do you rebase a branch?

 - You can rebase a branch using the command:
 > git rebase <branch-name>

6. What is a remote repository, and how do you add one?

 - A remote repository is a version of your project that is hosted on the internet or network. You can add a remote repository using the command:
 > git remote add <remote-name> <repository-url>

7. How do you push changes to a remote repository?

 - You can push changes to a remote repository using the command:
 > git push <remote-name> <branch-name>

8. How do you remove a file from Git without deleting it from your local file system?

 - You can remove a file from Git without deleting it from your local file system using the command:
 > git rm --cached <file-name>

9. What is the difference between git reset and git revert?

 - git reset moves the current branch pointer to a specified commit, optionally modifying the index and working directory to match.
 - git revert creates a new commit that undoes the changes of a specified commit, preserving the commit history.

10. How do you stash changes in Git?

 - You can stash changes using the command:
 > git stash

To apply stashed changes, use:
 > git stash apply

### Difficult Questions:
1. What is the purpose of git bisect?

 - git bisect is used to perform a binary search to find the commit that introduced a bug. You mark a known good commit and a known bad commit, and Git helps you identify the problematic commit.

2. How do you cherry-pick a commit?

 - You can cherry-pick a commit using the command:
 > git cherry-pick <commit-hash>

3. What is git reflog and how is it useful?

 - git reflog is a command that records updates to the tip of branches and other references. It is useful for recovering lost commits and understanding the history of branch tips.

4. How do you squash commits in Git?

 - You can squash commits using an interactive rebase:
 > git rebase -i <base-commit>

In the interactive editor, change pick to squash (or s) for the commits you want to squash.

5. How do you set up a Git hook?

 - Git hooks are scripts that run automatically on certain Git events. You can set up a Git hook by placing an executable script in the .git/hooks directory, such as pre-commit, post-commit, etc.

6. How do you handle large binary files in a Git repository?

Large binary files can be handled using Git Large File Storage (LFS). You can install Git LFS and track large files using:
 - git lfs install
 - git lfs track "*.bin"

7. What is the difference between git merge and git rebase?

 - git merge integrates changes from another branch into the current branch, creating a merge commit.
 - git rebase reapplies commits on top of another base commit, creating a linear commit history.

8. How do you perform a sparse checkout in Git?

Sparse checkout allows you to check out only a portion of the files in a repository. You can set it up using:
 - git sparse-checkout init --cone
 - git sparse-checkout set <directory>

9. What is the GIT_WORK_TREE environment variable used for?

 - GIT_WORK_TREE is used to specify the working directory for Git commands. It allows you to separate the Git repository (.git directory) from the working tree.

10. How do you use git filter-branch to rewrite commit history?

 - git filter-branch is used to rewrite commit history by filtering the branch. For example, to change the author of all commits:
 > git filter-branch --env-filter '
export GIT_AUTHOR_NAME="New Author"
export GIT_AUTHOR_EMAIL="newauthor@example.com"
' -- --all