## Branch and Merge

1. What is the command to create a new branch named `dev-food`?
    ```
    git checkout -b dev-food
    ```

2. What is the command to print what your current branch is?
    ```
    git branch
    ```


3. What command to list **all** branches including remote ones?
    ```
    git branch -r
    ```


4. What is command to switch your working copy to a branch named `dev-food`?
    ```
    git checkout dev-food
    ```

5. You commit some files to `dev-food` and try to "push" them to Github, but it fails:

    ```
    cmd>  git checkout dev-food
    cmd>  git push
    fatal:  The current branch dev-food has no upstream branch. 
    ```
    Explain this error.
    
    the local branch is not tracking the upstream.

6. What is the command to push `dev-food` to `origin` as a new remote branch on `origin`
    ```
    git push -u origin dev-food
    ```

7. Suppose your remote repository (Github or `origin`) has a branch named `beverages` that you don't have in your local repository.  What is the command to create a new local branch as a copy of the remote `beverages` branch that **tracks** the remote branch?
    There are many commands that do this.  For your own reference you may want to write several.
    
    Alternative 1
    ```
    git fetch origin
    git checkout beverages
    ```
    Alternative 2
    ```
    git fetch origin beverages
    git checkout beverages
    ```
    Alternative 3
    ```
    git fetch origin
    git checkout --track origin/beverages
    ```
    Alternative 4
    ```
    git fetch origin
    git checkout -b beverages origin/beverages
    ```
    Alternative 5
    ```
    git pull origin beverages
    ```


8. Consider this situation:
   - you have a local repository including a README.md file.
   - Your local repo is up-to-date with a remote Github repo (has identical README.md)
   - You edit README.md on Github using Github's web interface and save the changes.
   - On your local machine, you edit README.md, commit the changes and push it to Github. 
   
   What happens when you push?

   Explain why.
   
   I got the error : failed to push some refs to 'https://github.com/..../....'
   
   Because the Git Repository from Github and local does not match, so it is impossible to use git push to push README.md in the local repo to Github. 

    (Additional) How to fix:
    A local repository needs to get the latest updates from Github first. Use the 'git pull' command to update the local Git Repository to the current version.

### Additional
* list branches including remotes
    ```
    git branch -a  
    ```
* delete a local branch
    ```
    git branch -d <branchname>
    ```
* rename the current branch
    ```
    git branch -m <branchname>
    ```
* merge the commits from the given branch into the current branch
    ```
    git merge <branchname>
    ```