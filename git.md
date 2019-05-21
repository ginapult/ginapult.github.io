# Git Learnings

## Version Control

**Version Control System (VCS)** - a system that allows you to revisit various versions of a file or set of files by recording changes
+ **Local Version Control (LVC)**- one database on your hard disk that stores changes to files
+ **Centralized Version Control (CVCS)**
  + for collaboration within a developer team on a single file or set of files
  + a single server storing all changes and file versions, which can be accessed by various people
  + streamlines the collaboration process (by eliminating the need to involve all local databases)
  + allows programmers to have more knowledge of team members’ activities with certain files
  + gives administrators much more control over divvying up revision privileges
+ **Distributed Version Control (DVCS)**
  + addresses the major vulnerability of the CVS: the server as a single point of failure
  + allows people to create mirrored repositories; data backups easily placed on the server to replace any lost information
  + enables the use of various simultaneous workflows

## So, what is Git?

### Snapshots
Git is a DVCS that stores data in a file system made up of snapshots. Each time you save a changed version of your project — called **commit** — Git creates a snapshot of the file and stores a reference to it. If the file hasn't changed, Git only stores a reference to the already-stored identical version of it.

### Local Operations
Git mostly relies on local operations because most necessary information can be found in local resources. This allows for process expediency because a project’s history resides on the local disk, eliminating the need to fetch history information from the server, and allowing one to continue work on a project even when not online or on a VPN.

### Tracking Changes
Every single change applied to any file or directory is tracked by Git. And, as the gatekeeper, Git will always detect file corruption or loss of information in transit.

### Loss of Data
Git is set up to greatly minimize the possibility of irreversible damage to files, such as accidentally lost data. Git makes it extremely difficult for a snapshot of your file that is committed to be lost.

### States
Files in Git can reside in three main states
+ **Committed** - Data is securely stored in a local database
+ **Modified** - File has been changed but not committed to the database
+ **Staged** - Flagged a file’s changed version to be committed in the next snapshot

## History of Git
+ roots to the open source software project Linux kernel. 
+ Developers began using a DVCS called BitKeeper in 2002. 
+ In 2005, many of these developers stopped using this DVCS due to tension between the Linux kernel community and the company behind BitKeeper’s and the eventual revocation of the DVCS’ gratis status.
+ Linus Torvalds, the chief architect of the Linux kernel, began creating Git, with the intention of creating a DVCS with a workflow design similar to that of BitKeeper, which was also fast, Git allowed for non-linear development via multiple branches, could support large projects, possessed strong mechanisms preventing corruption, and had a simple design. 
+ Since its inception in 2005, Git has become one of the most utilized Version Control Systems in the world.

## Getting Started
+ Download and Install Git
+ Initial Customization
  + Configuration of Variables - An inherent Git tool called git config allows the setting of configuration variables that control aspects of Git’s operation and look.
+ Identity Setting - After installing Git, users should immediately set the user name and email address, which will be used for every Git commit.

Type the following into Terminal (Windows) or Command Line (Mac):

`git config --global user.name` "Jane Smith"
`git config --global user.email` "example@email.com"

To confirm that you have the correct settings, enter the following command:

`config --global user.name` (should return Jane Smith)
`git config --global user.email` (should return example@email.com)

*Using the –global option, these Git settings apply to anything on the system. To use different identity settings for a specific project, change the working directory to the desired local Git repository and repeat the steps above without using –global.

+ Set Default Text Editor - Without configuration of a default text editor, Git will use the system’s default editor–most likely Vim. To configure a different text editor, such as Emacs, type the following into your Terminal or Command Line: `$ git config --global` core.editor emacs

+ Check Settings
To check settings, use the `git config --list` command.

Example:

`$ git config --list
user.name=Jane Smith
user.email=example@email.com
color.status=auto
color.branch=auto
color.interactive=auto`
...

+ Getting Help - There are three ways to get more information on a particular command, by accessing the manual:

git help command
git command --help
man git-command

## Setting up a Git Repository
+ Importing - To import an existing project or directory into Git, follow these steps using the Terminal or Command Line:
  + Switch to the target project’s directory
Example:
`$ cd test` (cd = change directory)
Use the git init command
`$ git init`
Note: At this stage, you have created a new subdirectory named .git that has the repository files. Tracking has not commenced.

  + To start tracking these repository files, perform an initial commit by typing the following:
`$ git add *.c`
`$ git add LICENSE`
`$ git commit -m “any message here”`
Now, your files are tracked and there’s an initial commit. We will discuss the particular commands in detail soon.

## Cloning

### Clone
You can also create a copy of an existing Git repository from a particular server by using the clone command with a repository’s URL:
`$ git clone https://github.com/test`
By cloning the file, you have copied all versions of all files for a project. This command leads to the creation of a directory called “test,” with an initialized .git directory inside it, which has copies of all versions of all files for the specified project. The command also automatically checks out — or retrieves for editing — a copy of the newest version of the project.

To clone a repository into a directory with another name of your choosing, use the following command format:
`$ git clone https://github.com/test mydirectory`
The command above makes a copy of the target repository in a directory named “mydirectory.”

### Workflow
Local Repository Structure - The local Git repository has three components:

+ Working Directory: The actual files reside here.
+ Index: The area used for staging
+ Head: Points to the most recent commit

### Saving Changes
All files in a checked out (or working) copy of a project file are either in a tracked or untracked state.
+ Tracked - Tracked files can be modified, unmodified, or staged; they were part of the most recent file snapshot.
+ Untracked - Untracked files were not in the last snapshot and do not currently reside in the staging area.

*After cloning a repository, files have tracked status and are unmodified because they have been checked out but not edited.

## The Life Cycle of File Status
1. Edit File (Git flags it as modified because of changes made after previous commit.)
2. Stage the modified file.
3. Commit staged changes.

## Check File Status
To determine the state of files, utilize the git status command:
`$ git status`
On branch master
nothing to commit, working directory clean

*This information indicates which branch you’re on (we will cover branches in a later section) and states “working directory clean,” which means that files have tracked or modified status at the moment. Also, no untracked files are present because Git has not listed any.

## Tracking and Staging a New File
+ Single File - Track one file only by using the following format: `git add filename`
+ All Files - Track all files in a repository by using the following command: `$ git add *`
*After using these commands, files are tracked and staged for committing.

After adding a new file called EXAMPLE, you would see information regarding changes to be committed when using the git status command:

`$ git status`
On branch master
Changes to be committed:
  (use "git reset HEAD ..." to unstage)
new file: EXAMPLE
This information tells us that there are changes to be committed and that the file has been staged.

## Committing a File
After staging one or multiple files, you should commit the changes and record what you did within the commit message:

`$ git commit -m “made change x,y,z”`
*This step has committed changes for the file or files (you can have one commit message for multiple files, if applicable) to the HEAD.

## Committing All Changes
`$ git commit -a`
*This command commits a snapshot of all modifications to tracked files in the working directory.

## Pushing Changes
Next, you push changes to a remote repository.

Example:

`$ git push origin master`
*This command pushes changes from the local “master” branch to the remote repository named “origin”.

*For cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local repository. However, these names can be changed by the user.

## Stashing Changes
When you are not ready to commit changes but do not want to lose them either, `git stash` is a great option. This command temporarily removes changes and hides them, giving you a clean working directory. When you are ready to continue working on the changes, simply use the git stash apply command to retrieve the hidden changes.

## Remote Repositories
In order to collaborate on Git projects, you must interact with remote repositories, versions of a project residing online or on a network. You can work with multiple repositories, for which you can have read/write or read-only privileges. Teams can use remote repositories to push information to and pull data from.

## Cloned Repositories
As mentioned earlier, for cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local branch.
