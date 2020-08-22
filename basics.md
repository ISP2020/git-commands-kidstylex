## Git Basics

1. When working with Git locally, what are these?  Describe each one in a sentence
   * Staging area - directory for files and other transactions waiting to be added/deleted/updated in the repository. (the intermediate area in Git)
   * Working copy - contains both tracked files(files in repository) and untracked files(not included in repository).
   * master - the default branch name in Git.
   * HEAD - the pointer to the current branch reference.

2. A git commit includes the author's name and email.  How does git know your name and email?  When you install git on a new machine (or in a new user account) you should perform what 2 git commands?
    ```
   git config --global user.name "YOURNAME"
   git config --global user.email "YOURMAIL@email.com"

    ```
3. There are 2 ways to create a local Git repository.  What are they?
    - describe first way (one sentence)
    
        clone an existing Git repository from elsewhere.

    - describe second way
    
        create a local directory that you want to version control and turn it into a Git repository.


4. Suppose you create a git repository in a directory (folder) named "/project1". Where does git put the repository files for this project? Write the path to git's files.
    ```
    ../folder/project1/.git

    ```