# Codecadmey Notes: Unit 3 - Command Line and Git

## DAY ONE
### Lesson: Command Line Navigation

The command line is a text interface for your computer. It's a program that takes in commands which you type. These commands are then passed on to the computer's operating system to run.

To access the command line, we use a terminal emulator, often just called the terminal.

In the terminal, first you see $. This is called a shell prompt. It appears when the terminal is ready to accept a command.

##### REVIEW: 
The command line is a text interface for the computer's operating system. To access the command line, we use the terminal.

A filesystem organizes a computer's files and directories into a tree structure. It starts with the root directory. Each parent directory can contain more child directories and files.

From the command line, you can navigate through files and folders on your computer:
* `pwd` outputs the name of the current working directory.
* `ls` lists all files and directories in the working directory.
* `cd` switches you into the directory you specify.
* `mkdir` creates a new directory in the working directory.
* `touch` creates a new file inside the working directory.

## DAY TWO
### Lesson: Git Workflow

![Git Workflow][git-workflow]

A Git project can be thought of as having three parts:

1. A Working Directory: where you'll be doing all the work: creating, editing, deleting and organizing files
1. A Staging Area: where you'll list changes you make to the working directory
1. A Repository: where Git permanently stores those changes as different versions of the project

##### REVIEW:

Git is the industry-standard version control system for web developers.

Use Git commands to help keep track of changes made to a project:

* `git init` creates a new Git repository.
* `git status` inspects the contents of the working directory and staging area.
* `git add <filename>` adds files from the working directory to the staging area.
* `git add .` adds all files from the working directory to the staging area.
* `git commit -m <message>` permanently stores file changes from the staging area in the repository.

GitHub is a service for hosting remote repositories on the web.

* `git remote add origin <url>` specifies the remote repository using Git
* `git push -u origin master` pushes the changes to the master branch on the remote repository, linking the local repository to the remote repository.
* `git push origin master` pushes the changes to the master branch on the remote repository, given that the local repository and the remote repository are already linked.


<!-- Image Files -->

[git-workflow]: https://s3.amazonaws.com/codecademy-content/courses/learn-git/git_workflow.svg
