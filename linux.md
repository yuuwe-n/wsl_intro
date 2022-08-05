# basic linux
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

```
'ls -a'
'ls --all'
```

what you have just done is add a 'flag' or another name is called 'option'
'-a' is a flag
'--all' is also called a flag
'-a' and '-all' are equivalent flags, they both mean all, '-a' is just the shorthand'

you have added an option to 'ls' which allows you to "list all" the stuff in your current directory
usually the 'ls' command hides files with files that have the symbol "dot" in front of the file such as ".ssh" ".config"

this is what you'll need to know for the basic syntax for all linux commands:
\> command -flag argument
you add '-flag' or '--flag' to add more functionality to a command

## navigation

now that we have a basic undestanding of terminal syntax, we have basic navigation now

with the 'cd' command
just doing 'cd' with no arguments get you into the home directory
within the os, you can find many directories, if you do
```
cd /
ls
```

you will enter the "root" directory", this is where everything enlies,
you see /bin, /etc/, /tmp, all these other directorys, ignore them

now if you do, 
```
cd /home/
ls
cd username
ls -a
```

you will see that you were in the dir you were just in at first called the "home directory"
this home directory is where you login at all times

what you saw earlier is where the os puts stuff neccessary to be an os,
the home directory is where you should be developing etc.
you saw that cd without any arguments goes to the home directory

if you want to go back to the /home/ directory, you can do
`cd ../`

what this command does, is go back a directory
"." refers to your current working directory (also equivalent to "./")
".." refers to your past directory (also equivalent to "../")

so if you are in /home/username/
doing 'cd ../' goes back a directory to "/home"
if you do 'cd../" again, it goes back to "/" (root dir)

you can also do 'cd' again to go back to your home dir (home dir refers to /home/username)

there are special arguments other than the ones you've just seen,
these special arguments can be used for any command 
```
'.': refers to current working dir
'..': refers to previous directory
'~': refers to your home directory
'-': refers to the last directory you've been in (different from '..')
```


