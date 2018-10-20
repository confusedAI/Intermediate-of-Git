### git revert
The **git revert** command figures out how to invert the changes introduced by a particular commit and appends a new commit with the resulting inverse content. This prevents Git from losing history, which is important for the integrity of your revision history and for reliable collaboration.<br/>
Reverting should be used when you want to undo the changes made during some commit from your project history.This can be useful, for example, if you’re tracking down a bug and find that it was introduced by a single commit. Instead of manually going in, fixing it, and committing a new snapshot, you can use **git revert** to automatically do all of this for you.

### How it works
Other 'undo' commands like, **git checkout** and **git reset**, move the HEAD and branch ref pointers to a specified commit. Git revert also takes a specified commit, however, **git revert** does not move ref pointers to this commit. A revert operation will take the specified commit, inverse the changes from that commit, and create a new "revert commit". The ref pointers are then updated to point at the new revert commit making it the tip of the branch.

**git revert HEAD**<br/>
This will revert the latest commit. This is same behavior as if we reverted to second last commit. A revert will create a new commit which will open up the configured system editor prompting for a new commit message. Once a commit message has been entered and saved Git will resume operation. We can now examine the state of the repo using **git log --oneline** and see that there is a new commit added to the previous log.
