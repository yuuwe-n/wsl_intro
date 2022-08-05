# wsl_intro
introduction to wsl for developers

table of contents

1. basic linux commands/why development much easier
2. how git works for developers
3. vscode integration/ how it works with wsl
4. markdown
5. starting to work with go documentayion with wsl (go lang has documentation with terminal so thats why i wanted to introduce wsl to you rn)
6. getting everything integrated: vscode, with go, with git 

# basic linux
follow instructions to install [wsl](https://docs.microsoft.com/en-us/windows/wsl/install)

basics of what wsl is:
wsl (windows subsystem for linux) allows it for a developer to access linux from windows.
once you have created an acct for ubuntu on your wsl shell, you will be greeted by 

```
user@hostname $
```

from here you can enter commands such as (sidenote ignore the apostrophes ' ' when entering commands)
'ls' : "lists" the content of the directory you are in currently

'cd' : "change directory" allowing you to go into a directory, meaning u can enter a directory

'mkdir' : "make directory" self explaintory

try getting used to going to directories and listing the content of directories

exercise:
1. list the contents of the directory u are currently in
2. make a new directory named whatever u want (mkdir dirname)
3. change your directory to the new one you've created (cd dirname)

after you've done that, you can see there is nothing in that new directory u just made
try putting some stuff in there
'touch' create a file 

'nano' edit a file

exercise:
1. create a file (touch filename)
2. edit that file (nano filename)

once you're in that file, ignore the bottom for now, just put whatever you want in that file (ignore the \<\> when doing keybinds)
to save, do the command \<Ctrl + O\>
to exit, do the command \<Ctrl + X\>

you can find your file by using the 'ls command'
if you type 'cd' without any arguments, you will go to your home directory ( i will explain home directory later )

through these exercises you have seen:
\> command argument
this is the basic syntax for doing commands in linux

try doing:
'ls -a'
'ls --all'

what you have just done is add a 'flag' or another name is called 'option'
'-a' is a flag

you have added an option to 'ls' which allows you to "list all" the stuff in your current directory
usually the 'ls' command hides files with files that have the symbol "dot" in front of the file such as ".ssh" ".config"

this is what you'll need to know for the basic syntax for all linux commands:
\> command -flag




# git

# vscode integration

# markdown

# go/wsl

# integration
