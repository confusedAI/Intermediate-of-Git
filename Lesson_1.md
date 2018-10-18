### Git is a distributed version control system.<br/>
With Git, you can easily follow your source code's revision history and track changes. You can also go back in time to learn about how the version has changed and who has made the changes. When the latest version of a file is on a shared repository, Git will prevent unintentional overwrites by anyone on your team who has an older version of the file.<br/>

There are four main components of a Git project:
 * __Git Repository__ -- The repository, or repo, is the “container” that tracks the changes to your project files. It holds all the commits (a snapshot of all your files at a point in time) that have been made. You can access the commit history with the command **git log**

 * __Working tree__ -- The working tree, or working directory, consists of files that you are currently working on. The working directory is a version of a particular commit, a particular snapshot of a project that you checked out. It is the version of your Git history that HEAD is pointing at, at any given moment.
"Checked out" means that you have the decompressed versions of files that were pulled out of your Git repository, available for editing.

 * __Index__ -- The index, or staging area, is where commits are prepared.Essentially, the contents of the index are what will go into the new commit. **git add** command will add or update files from the working tree into your index.

 * __Head__ --- HEAD is the part of git that points to your branches _(the master branch by default)_. HEAD points to the currently checked out branch, and that in turn points back to the last commit from that branch. HEAD can move not only in time (when you check out previous commits), but it also moves when you create new branches or simply switch to other branches.It's also the point in your Git history that you can place your next commit upon, the parent for your next commit.So, in effect, HEAD is a reference that frequently changes and points to two things: the branch itself, and through that, the last commit on that branch.


### The basic Git workflow goes something like this:

 1. Modify files in your working tree.

 2. Stage the changes you want to be included in the next commit.

 3. Do a commit, which takes the files as they are in the staging area and stores that snapshot permanently to your Git repository.

You can probably guess from the Git workflow, files can be in one of three states:

  * Modified  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-- In working tree
  * Staged      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -- In staging area
  * Committed   &nbsp;&nbsp;-- In git repository

When a file is first modified, the change can only be found in the working tree. You must stage the changes you want to be included in your next commit. The index contains all file changes that will be committed. Once you have finished staging files, commit them with a message describing what you changed. The modified files are now safely stored in the repository.

   ![Alt text](image1.png?raw=true)


Also notice that each file in your working directory can be in one of two states: tracked or untracked. Tracked files are files that were in the last snapshot; they can be unmodified, modified, or staged. In short, tracked files are files that Git knows about.

Untracked files are everything else — any files in your working directory that were not in your last snapshot and are not in your staging area. When you first clone a repository, all of your files will be tracked and unmodified because Git just checked them out and you haven’t edited anything.
As you edit files, Git sees them as modified, because you’ve changed them since your last commit. As you work, you selectively stage these modified files and then commit all those staged changes, and the cycle repeats.
