# All About Git

Reading assignment 'Read03'

## Questions & Answers

1. What is Version Control? A system that allows you to revisit various versions of a file by recording the changes made rather than creating an entirely separate file. It grants the ability to see which individuals made what changes, allowing mistakes to be taken care of easily.
2. What is `cloning` in Git? It is the act of retrieving a mirrored copy of a repository to work on in your own local space.
3. What is the command to track and stage files? `git add [filename]` for individual file/s or `git add .` for to track and stage all files.
4. What is the command to take a snapshot of your changed files? `git commit -m ""` will take the snapshot and you can add some text to explain your reasoning to the changes made.
5. What is the command to send your changed files to Github? `git push origin main` This command pushes changes from the local “master” branch to the remote repository named “origin".

## Notes

Here are the notes I've taken while reading the following blog:

[Git Tutorial](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/)

### Version Control

VCS

A system that allows you to revisit various versions of a file by recording the changes made rather than creating an entirely separate file. It grants the ability to see which individuals made what changes, allowing mistakes to be taken care of easily.

#### Local Version Control

Local VCS

A database that stores changes to files locally.

#### Centralized Version Control

CVCS

A single server stores changes and file versions that can be accessed by various people, streamlining the collaboration process.

#### Distributed Version Control

DVCS

Similar to a CVCS, which streamlines collaboration, a DVCS allows multiple individuals to create mirrors of repositories to store locally on their respective hard drives. Any changes made locally can then be requested to be sent back to the main server. This prevents the potential of a single point of failure from making changes within the same server.

### What is Git?

> Git is a DVCS that stores data in a file system made up of snapshots.

Each time a change is made within a repository, known as a 'commit,' Git takes a snapshot of the changes and saves a reference to it.

#### Local Operations

This allows an individual to work on a project offline. Git eliminates the need to fetch information from the server every time an individual wants to work or make changes.

#### Tracking Changes

Every change applied anywhere within a repository, Git will keep track of.

#### Loss of Data

> Git makes it extremely difficult for a snapshot of your file that is committed to be lost.

#### States

Three main states: committed, modified, and staged.

##### Committed

Data stored on the local hard drive.

##### Modified

Changes have been made but not committed.

##### Staged

Acknowledged changes made to be committed in the next snapshot.

### History of Git

> Git traces its roots to the open source software project Linux kernel. Developers of this project began using a DVCS called BitKeeper in 2002. In 2005, many of these developers stopped using this DVCS due to tension between the Linux kernel community and the company behind BitKeeper’s and the eventual revocation of the DVCS’ gratis status. Subsequently, Linus Torvalds, the chief architect of the Linux kernel, began creating Git. With the intention of creating a DVCS with a workflow design similar to that of BitKeeper, which was also fast, Git allowed for non-linear development via multiple branches, could support large projects, possessed strong mechanisms preventing corruption, and had a simple design. Since its inception in 2005, Git has become one of the most utilized Version Control Systems in the world.

### How to use Git

#### Cloning

Copy all version of all files for a project to your local hard drive.

`git clone [link to Git repository]`

Clone a repositry with a different name.

`git clone [link to Git repository] [different name]`

#### Work Flow

Three components:

- Working Directory: where the files reside
- Index: Area used for taging
- Head: Points to the most recent commit

#### Saving Changes

##### Tracked

Tracked files can be modified, unmodified, or staged.

##### Untracked

Untracked files were not in the last snapshot and do not currently reside in the staging area.

#### Life Cycle of File Status

1. After an edit, Git flags it as modified as changes were made after the previous commit.
2. You stage the new modified file. 
3. Commit the staged changes.

### File status

`git status`

Determines the state of files.

### Tracking and Staging a New File

`git add [filename]`

tracks one file

`git add .`

tracks all flagged changes

### Committing a File

`git commit -m "changes made because..."`

Commit changes and record **why** you made these changes.

### Pushing Changes

`git push origin master`

Pushes changes to the remote repository.

>*This command pushes changes from the local “master” branch to the remote repository named “origin”.

>For cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local repository. However, these names can be changed by the user.

### Stashing Changes

`git stash`

Command that temporarily removes changes and hides them, giving a clean working directory.

`git stash apply`

Command to retrieve the previous hidden changes.
