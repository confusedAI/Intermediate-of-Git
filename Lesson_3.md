### Undoing changes
One of the most valuable features of Git is the ability to undo mistakes.<br/>
A fun metaphor is to think of Git as timeline management utility. Commits are snapshots of a point in time or points of interest along the timeline of a project's history. Additionally, multiple timelines can be managed through the use of branches. When 'undoing' in Git, you are usually moving back in time, or to another timeline where mistakes didn't happen.

One of the best utilities for reviewing the history of a Git repository is the **git log --oneline** command. Each commit has a unique SHA-1 identifying hash. These IDs are used to travel through the committed timeline and revisit commits. By default, **git log --oneline** will only show commits for the currently selected branch.Invoking the command **git branch -a** will return a list of all known branch names. One of these branch names can then be logged using **git log ~~branch_name~~**.

### git checkout
**git checkout ~~commit id~~** is an easy way to “load” any of the saved snapshots onto your development machine. During the normal course of development, the HEAD usually points to master or some other local branch, but when you check out a previous commit, HEAD no longer points to a branch—it points directly to a commit. This is called a “detached HEAD” state.<br/>

If you haven't made any commits yet, you can leave detached head state by simply checking out whichever branch you were on before checking out the commit sha:<br/>
**git checkout ~~branch~~**

If you did make commits while you were in the detached head state, you can save your work by simply creating a new branch before you leave detached head state:<br/>
~~Checkout a new branch at current detached head state~~<br/>
**git checkout -b ~~newBranch~~**

<br/>_Example:_
![Alt text](image2.png?raw=true)
