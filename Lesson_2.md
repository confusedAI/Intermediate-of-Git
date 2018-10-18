There are two types of Git repositories: remote and local.
* A remote repository is hosted on a remote server that is shared among multiple team members.
* A local repository is hosted on a local machine for an individual user.

There are two ways to create a local repository on your machine. You can create a new repository from scratch by creating a folder on your computer or clone an existing repository.

* **Git init**<br/>
It can be used to introduce Git into an existing, unversioned project in order to start tracking changes.

* **Git clone**<br/>
Use this command to copy a remote repository onto your local machine.

> **Note:** By default, git clone automatically sets up a local master branch that tracks the remote master branch it was cloned from.A cloned repository has the same history log as the original one. You can refer and backtrack to any of those commits within your local repository.

It is important to note that Git does not automatically save every change you make. You must tell Git which changes you want to be recorded by staging those changes. After staging, you can commit the changes so that they are recorded in the repo.
### Making changes
Changes are made in the working tree—a directory consisting of the files you are currently working on. The working tree is where you edit files, add new files, and remove files that are no longer needed.

All files that are changed in the working tree are noted as modified in the index. An index is a staging area where new commits are prepared. It sits between the repository and working tree.

Changes made in the working tree will not be saved directly to the repository. All changes must first be staged in the index in order to be saved in the repo. Only the files in the index are committed to the repo.

_When committing your changes, you are required to enter a commit message. The commit message should provide descriptive comments regarding the changes you have made_.

__A 40-character checksum hash is used to uniquely identify a commit. You can use this checksum hash to retrieve the status or changes of files and directories that were made on the given commit in your repository.__
