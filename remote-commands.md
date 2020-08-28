## Commands for Remotes

1. The command to list all your remote repositories, with their URL.
     ```
     git remote -v
     ```

2. The command to view details about a remote repo named origin, including all the remote banches, and local tracking branches.
     ```
     git remote show origin
     ```

3. Suppose your remote repository (Github or `origin`) has a branch named `beverages` that you don't have in your local repository.  What is the command to create a new local branch as a copy of the remote `beverages` branch that **tracks** the remote branch?
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

4. Consider this situation:
   - you have a local repository including a README.md file.
   - Your local repo is up-to-date with a remote Github repo (has identical README.md)
   - You edit README.md on Github using Github's web interface and save the changes.
   - On your local machine, you edit README.md, commit the changes and push it to Github. 
   
   What happens when you push?

   Explain why.
   
   I got the error : failed to push some refs to 'https://github.com/..../....'
   
   Because the Git Repository from Github and local does not match, so it is impossible to use git push to push README.md in the local repo to Github. 

5. What are the steps to resolve the problem in the previous problem?
    * step one 

        Use 'git pull' command to update the local Git Repository to the current version.
        ```
        git pull origin <brandname>
        ```
    * step two

        Use 'git push' command to upload local repository content to a remote repository.
        ```
        git push origin <brandname>
        ```

6. Suppose you want to move origin to a different URL. This can happen if you change the name of a repo on Github, or transfer ownership from one person to another. What is the command to change the URL for origin to https://github.com/your_name/newrepo.
    ```
    git remote set-url origin https://github.com/your_name/newrepo.git
    ```