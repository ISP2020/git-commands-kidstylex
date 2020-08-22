### Adding and Changing Stuff

Suppose your working copy of a repository contains these files and directories:
```
README
out/
     a.exe
src/ a
     b
	 c
test/
     d
```     

1. What is the command to add README and *everything* in the `src` directory to the git staging area?
     ```
     git add README src/*
     ```

2. Write the command to add `test/d` to the staging area.
     ```
     git add test/d
     ```

3. Write a command to list files in the staging area.
     ```
     git diff --name-only --cached
     ```

4. You decide you **don't** want to add `test/d` to git.  Write the command to remove `test/d` from the staging area.
     ```
     git rm --cached test/d
     ```

5. Write the command to commit the staging area to the repository.
     ```
     git commit -m "[msg]"
     ```

6. You **never** want any files in the `out/` directory to be commited to git. Describe 2 steps to configure git for this:
     * step one 
     
         create a .gitignore file to ignore `out/` directory.
     ```
     .
     .
     # Ignore the build directory
     /out
     .
     .

     ```

     * step two
     
         add, commit, and push a .gitignore file to the repository.


7. What is the command to move `a`, `b`, and `c` from the `src` directory to the top-level directory of the project, so that they are also moved in the git repository?
     ```
     git mv src/* ~/../[projectfolder]/
     ```

8. Commit this change with the message "moved src directory".
     ```
     git commit -m "moved src directory"
     ```

9. If you change a **lot** of files, using `git add` for each one can be tedious.  Write a command to add *all modified files* to the staging area.   
    (After doing this you should use "git status" to verify you didn't add unintended files.)
    ```
    git add -u
    ```


10. What is the command to delete the file `c` from both your working copy **and** the repository? (This stages the change but it is not deleted from repo until you commit it.)
    ```
    git rm src/c
    ```

11. What is the command to show all differences between your working copy and the most recent commit? (Can be kind of hard to read.)
    ```
    git diff HEAD
    ```