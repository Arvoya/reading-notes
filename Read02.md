# The Coder's Computer

Reading assignmnet 'Read02'

## Questions & Answers

1. What are four important features to look for in a text editor? Top four features are: code completion, syntax highlighting, variety of themes, and offers wide selection of extensions.
2. What do the following commands do.
    - `pwd` - prints the current directory you are in.
    - `ls` - creates a list of the files or directories relative to current directory
    - `cd` - changes location of current directory
    - `mkdir` - makes a new directory
    - `touch` - makes a new file
3. Can you explain what is happening in the following scenario if these commands and arguments are entered into the command line? (Arguments are extra instructions given to a command.)
    - `cd projects` - changing to a directory known as 'projects'.
    - `mkdir new-project` - creates a new directory names 'new-project'
    - `touch new-project/newfile.md` - creates a file titled 'newfile.md' within the directory 'new-project'
    - `cd ..` - goes back to the parent directory
    - `ls projects/new-project` - creates a list of the files or directories found within the directory 'new-project' that is the child of the directory titled 'projects'.

## Notes

Here are the notes I've taken while reading the following blogs:

[Choosing a Text Editor](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://codefellows.github.io/code-102-guide/curriculum/class-02/Choosing-A-Text-Editor--The-Older-Coder.pdf) \|
[The Command Line](https://ryanstutorials.net/linuxtutorial/commandline.php)
\| [Basic Navigation](https://ryanstutorials.net/linuxtutorial/navigation.php) \| [About Files](https://ryanstutorials.net/linuxtutorial/aboutfiles.php)

### Choosing a Test Editor

#### Picking the best

- It doesn't matter which text editor you use.
- The one you enjoy using is the best for you.

#### What is a text editor

- One of the most important tools for a web developer.
- Allows you to write and manage text, especially text that is used to build a website.

#### Features to look for

> Good programmers are lazy programmers

- code completion
- syntax highlighting
- variety of themes
- offers wide selection of extensions

### The Command Line

> Your window into the computer

#### What is it?

- a text based interface to the system
- aka terminal

#### How it works

- it presents you with a prompt
- awaits a specific command
- runs the command
- returns to a prompt

#### The Shell

- Shells are part of the operating system that governs how the terminal behaves.
- When I run the command
`echo $SHELL` it shows up as 'zsh' so that is the shell I'm using

### Basic Navigation

- `pwd` - Print Working Directory \| tells you what your current or present working directory is.
  - when I type this command I'm shown "/home/arvoya/projects/courses/code-102/Class02" showing the exact file (or path) I am currently working in.
- `ls` - short for 'List'
  - Shows a list of files or other directories found within the current directory.

#### Paths

2 types of paths:

- Absolute - these paths specify a location in relation to the root directory
  - begins with a forward slash (/)
- Relative - these paths specify a location in relation to where we currently are in the system
  - does not begin with a forward slash

The file system is a hierarchical structure.

- The top of the structure is known as the **root** directory. 
- The root is denoted by a single slash (/)
- `~` - shorcut for home directory
- `.` - reference to your current directory
- `..` - reference to the parent directory
- `cd` \[location] - a command to change location to specified target
  - on its own `cd` will bring you back to the root directory

### About Files

> Everything is actually a file. A text file is a file, a directory is a file, your keyboard is a file (one that the system reads from only), your monitor is a file (one that the system writes to only) etc.

#### File extension

- a set of 2 - 4 characters that denote what type of file it is. 
  - file.exe - executable file (program)
  - file.txt - plain text file
  - file.png, file.gif, file.jpg - images
- `file` \[path] - will tell you what type of file it is

#### Case Sensitive

- Possible to have two or more files and directories with the same name but letters of different case. 
  - File.txt
  - FILE.txt
  - file.txt

#### Spaces in names

- It is possible to have spaces in names of files, but the terminal will need additional help. 
  - `cd Holiday Photos` could result in an error saying `Holiday: No such file or directory`
  - `cd 'Holiday Photos'` would fix the error by using single or doublt quetoes. 
  - `cd Holiday\ Photos` would also work because the backslash key (\\) nullifies or 'escapes' the special meaning of the next character. In this case the space.

#### Hidden Files

- If a file or directory's name begins with a (.) known as a fullstop, then it is considered to be hidden. 
- `ls` - as mentioned before is list 
  - if we add `-a` to make `ls -a` the terminal will list all files, including hidden ones.
