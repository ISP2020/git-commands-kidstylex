## Using Git

> 1. Answer these questions using Markdown.  
> 2. Delete these instructions.    
> 3. Check that your formatting is correct (points deducted if incorrect).  VS Code and IntelliJ have markdown previewers.
> 4. Optional: For your own reference you may optionally do the following:
>    * Divide this file into separate Markdown files for each section, and put a link to each file in README.md.
>    * Add additional sections or questions to the end for things you'd like to remember.

> To display your answers as lines of *unformatted text* (like HTML `<pre>` tag) there are 2 ways to do it:
> - leave 4 spaces at start of the line (and the text on the line must not "look like" a Markdown numbered or bulleted item)
> - put the lines between triple backquotes (as in the source code for this file):    
    ```
    unformatted text
    ```
* [Git Basics](basics.md)
* [Adding and Changing Stuff](addingandchanging.md)
* [Branch and Merge](branchandmerge)
* [Using Git](undoing.md)


## Viewing Changes and Commits

* Command to show the history of a repository in the terminal (command) window.  This form shows one line per commit, with a graph, and all branches.
    ```
    git log --oneline --graph --all
    ```
    Some versions of git have an *alias* "log1" for this (`git log1`).

* The GUI tool `gitk` or `gitk --all` displays even more info about the commit history.


* The output of `git diff` can be hard to read. To view differences more visually:

    1. View differences on Github.
    2. Meld or Diffuse to compare and merge files. `git difftool` lists more tools.
    3. `gitk` shows diffs between commits
    4. Eclipse EGit shows side-by-side diffs and can merge interactively

---
## Resources

[Learn Git Interactive Tutorial][LearnGitInteractive] excellent visual tutorial.   
[Git Visualizer][VisualizeGit] execute Git commands and see the results as a graph.    
[Pro Git Online Book][ProGit]    
[Pro Git PDF][ProGitPdf] free download

[ProGit]: https://www.git-scm.com/book/en/v2 "Pro Git online book on Git-scm.com"
[ProGitPdf]: https://progit2.s3.amazonaws.com/en/2016-03-22-f3531/progit-en.1084.pdf "Pro Git v.2 PDF on AWS. Longer, book format."
[LearnGitInteractive]: https://learngitbranching.js.org "Interactive graphical git tutorial"
[VisualizeGit]: http://git-school.github.io/visualizing-git/ "Online tools draws a graph of commits in a repo, as you type"
