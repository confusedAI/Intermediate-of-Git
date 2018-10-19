### Undoing changes
One of the most valuable features of Git is the ability to undo mistakes.<br/>
A fun metaphor is to think of Git as timeline management utility. Commits are snapshots of a point in time or points of interest along the timeline of a project's history. Additionally, multiple timelines can be managed through the use of branches. When 'undoing' in Git, you are usually moving back in time, or to another timeline where mistakes didn't happen.

One of the best utilities for reviewing the history of a Git repository is the **git log** command. Each commit has a unique SHA-1 identifying hash. These IDs are used to travel through the committed timeline and revisit commits. By default, **git log** will only show commits for the currently selected branch.Invoking the command **git branch -a** will return a list of all known branch names. One of these branch names can then be logged using **git log ~~branch_name~~**.
