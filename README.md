# MiniGit
MiniGit is an implementation of a version-control system. This version-control system mimics some of the basic features of the popular version-control system git. The supported functionalities are
  - init
  - add
  - commit
  - rm
  - log
  - global-log
  - find
  - status
  - checkout
  - branch
  - rm-branch
  - reset
  - merge

### Team Member
- Bruk Argaw
- Omid Khosravani

# Tools
  - Java
  - eclipse :- IDE
  - Git
  - Github

## Features
1. Saving backups of directories of files. In minigit, this is called committing, and the backups themselves are called commits.
2. Restoring a backup version of one or more files or entire commits. In minigit, this is called checking out those files or that commit.
3. Viewing the history of your backups. In minigit, you view this history in something called the log.
4. Maintaining related sequences of commits, called branches.
5. Merging changes made in one branch into another.

## Directions To Use MiniGit
 1. clone the repo
 2. go the directory that contains repo and run minigit
 3. commands (note:- you must run init before and other minigit command)

#### Commands
- init :- Creates a new minigit version-control system in the current directory
            * Usage: ~~~ java MiniGit init ~~~

- add : Adds a copy of the file as it currently exists to the staging area
            * Usage: ~~~ java MiniGit add [file name] ~~~

- commit :-  Saves a snapshot of certain files in the current commit and staging area so they   can be restored at a later time, creating a new commit.
            * Usage: ~~~ java MiniGit commit [message] ~~~

- rm :- Untrack the file
            * Usage: ~~~ java MiniGit rm [file name] ~~~

- log :-  Starting at the current head commit, display information about each commit backwards along the commit tree until the initial commit.
            * Usage: ~~~ java MiniGit log ~~~

- global-log :- Like log, except displays information about all commits ever made.
            * Usage: ~~~ java MiniGit global-log ~~~

- find :- Prints out the ids of all commits that have the given commit message, one per line.
            * Usage:  ~~~ java  MiniGit find [commit message] ~~~

- status :- Displays what branches currently exist, and marks the current branch with a 'star'. Also displays what files have been staged or marked for un-tracking.
            * Usage: ~~~ java  java MiniGit status ~~~

- checkout :-  There are 3 possible use cases
    1. Take the version of the file as it exists in the head commit, the front of the current     branch, and puts it in the working directory, overwriting the version of the file that's already there if there is one.
            * Usage: ~~~ java  MiniGit checkout -- [file name]~~~

    2. Takes the version of the file as it exists in the commit with the given id, and puts it in the working directory, overwriting the version of the file that's already there if there is one. The new version of the file is not staged.
             * Usage: ~~~ java MiniGit checkout [commit id] -- [file name]~~~
    3. Takes all files in the commit at the head of the given branch, and puts them in the working directory, overwriting the versions of the files that are already there if they exist. Also, at the end of this command, the given branch will now be considered the current branch (HEAD). Any files that are tracked in the current branch but are not present in the checked-out branch are deleted.
              * Usage: ~~~ java MiniGit checkout [branch name] ~~~
- branch :-  Creates a new branch with the given name, and points it at the current head node
              * Usage: ~~~ java MiniGit branch [branch name] ~~~
- rm-branch :- Deletes the branch with the given name
              * Usage: ~~~ java MiniGit rm-branch [branch name] ~~~
- reset :- Checks out all the files tracked by the given commit
              * Usage: ~~~ java MiniGit reset [commit id] ~~~
- merge :- Merges files from the given branch into the current branch
              * Usage: ~~~ java MiniGit merge [branch name] ~~~

![Alt Text](https://github.com/bkargaw/MiniGit/blob/master/assets/split_point.png)

## Future Directions
- Objective:-  Going Remote allow the ability to save files from the local version to a remote version. This will try to mimic the popular online repo Github.The new functionalities will be...  
    * add-remote :-  Saves the given login information under the given remote name
    * rm-remote :- Remove information associated with the given remote name.
    * push :- Attempts to append the current branch's commits to the end of the given branch at the given remote
    * fetch :- Brings down commits from the remote minigit into the local minigit.
    * pull :- Fetches branch [remote name]/[remote branch name] as for the fetch command, and then merges that fetch into the current branch.
