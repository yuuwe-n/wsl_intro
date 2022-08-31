# wsl_intro

introduction to wsl for developers

**table of contents**

1. **[linux](#linux)**: basic linux knowledge to get stuff working
2. **[git](git.md)**: how git works for developers
3. **[editors](vscode.md)**: integration with wsl
4. **[markdown](markdown.md)**: basic markdown, for documentation etc.
5. **[go](go.md)**: starting to work with go commands with wsl (go lang has documentation with terminal so thats why i wanted to introduce wsl to you rn)
6. **[integration](integration.md)**: getting everything integrated: vscode, with go, with git 
# linux

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

```
exercise:
1. list the contents of the directory u are currently in
2. make a new directory named whatever u want (mkdir dirname)
3. change your directory to the new one you've created (cd dirname)
```

after you've done that, you can see there is nothing in that new directory u just made
try putting some stuff in there

'touch' create a file 

'nano' edit a file

```
exercise:
1. create a file (touch filename)
2. edit that file (nano filename)
```

once you're in that file, ignore the bottom for now, just put whatever you want in that file (ignore the \<\> when doing keybinds)
to save, do the command \<Ctrl + O\>
to exit, do the command \<Ctrl + X\>

you can find your file by using the 'ls command'
if you type 'cd' without any arguments, you will go to your home directory ( i will explain home directory later )

through these exercises you have seen:

`$ command argument`

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

`$ command -flag argument`

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

i can use these with other commands like 'ls', 'mkdir' etc.
```
'ls ../' : lists previous directory
'ls /' : lists root directory
'mkdir ~/test' : makes directory in home directory called test
'cd /home/username/test' changes directory  to test
'cd ~/test' equivalent to previous command

'cd /': goes to root
'cd ~': goes to home
'cd -': if you do this command, it will go back to root
```

## general linux 
there are some other important commands in linux such as
`man` : manual
`man man` : just browse some of the documentation in there

so 'man', allows you to know what command something is
'man command'

use the \<page up\> and \<page down\>  to go up/down a page
OR use \<CTRL + u\> and \<Ctrl + D\> to go half a page up/down
```
man ls
man cd
man mkdir
```
if you want to know anything, like the options like earlier 'ls -a', use the man command
if you want to actually learn linux outside the basic commands i recommend using the man
pages for everything. if you don't know the command name use. basically searches
for manual pages
`man -k` OR
`apropos` (these mean the same thing)

`man -k hier` : you can find stuff related to hierarchy

this manual is a good intro to how linux is structured
`man hier`

## ubuntu
im not gonna get much into distributions, but all you need to know is that there are different OS's of linux like
Ubuntu called distributions

there are minor differences between distributions, but all you need to know is that you are using ubuntu

ubuntu has some differences like for install packages.

to install stuff, you cant just install the exe in general for linux. (exe is for windows, even macOS has a different
way to install software)

> this is about linux for development purposes, there is other ways to install/other info for desktop use, but we dont go into that here. not many developer tools need to install tar archives, or use a gui to install (we are using WSL)

you have to use a command

`sudo apt-get install package_name`

try doing it with python3, 

`sudo apt-get install python3`

## tips
also big tip: use the \< tab \> to autocomplete dir names, file names, etc

linux is case sensitive so "test" and "Test" are different

compared to windows, you can use include most symbols to name stuff, but there are some special symbols,
so I don't recommend you use special characters

also if you have a name that has a space, you can either do '\ ' or enclose the argument with "double quotes"

use the \<up> and \<down> arrow, to get previous commands

use \<Ctrl + R \> to reverse search previous commands, u can use \<Ctrl +R\>, and \<Ctrl + shift + R\> to scroll through results

---


that is basically all you need to know to do develop with linux
you should go to the next page [git](git.md)

# git

i recommend skimming through the man doc for git
`man git`

in the manual it says to go to for more information
[https://git-scm.com/docs](https://git-scm.com/docs)

once you should at least have a basic understanding of how the source management system git works

here are some commands that you will be making very often however:

`git clone repourl` : clones a repository (can find more info in the section about [git clone](#git_clone))

```
git add .
git commit -m "message"
git push
```
for a basic understanding:

`git add .` means add the current changes for the '.' current directory, remember that'.' means current directory

`git commit -m "message"` means commit the current changes under a commit called "mesage"

`git push` sends the commit to the git repo,

if you want to just do offline edits, you can just do `git add .` and `git commit -m "message`
for local development, these allow you to track changes with these 2 commands

## git_clone
> this is assuming you are goin to use github for your repo server
you can either clone with https or ssh, cloning/pushing code with https is depricated now
it is now recommended that you use ssh since it is secure

`man ssh` is recommended

ssh is a authentication protocal 
it allows you to remotely access machines 

ssh with git allows you to basically to get code from a server and be able to push and manage it using git
within ssh, it uses ssh keys, which uses a public and private key (learn more from the [official ssh website](https://www.ssh.com/academy/cryptography/private-and-public-keys) )

i believe https is depricated since it maybe less secure to authenticate with github
ssh is recommended since it uses keys

to get a key, do
`ssh-keygen` : i recommended pressing \<Enter\> for each option, unless you know what you are doing (meaning
you know you won't lose your password/know how to enter a custom location for your key for auth)

if you try now doing

`git clone ssh@ssh`: it will not work since you havent copied your public ssh key to github
you must copy your public key to github for github to know this is you

go to github settings to ssh and add a key
you can do the command

`cat ~/id_rsa.pub` : outputs your public key in plain text

you can now highlight the stdout and do \<Ctrl + Shift + C \> to copy the output

add the required content, and name it whatever you want (recommended to do the name of your computer, its 
honestly just for youself to know which computer you are sshing from)

also `cat` is a new command meaning concatanate, do `man cat` if you want to learn more

you can now git clone your repo
there may be other steps with 'git config --global ...', but i trust you are capable of doing that

---

this is all you need to know with git, now you can move onto [vscode](vscode.md)

# vscode

follow these steps to get vscode to work with wsl [wsl-vscode](https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode)

i am not on windows or linux rn (openbsd gang), so i don't even have vscode, but here is what i am assuming

in wsl, you can use `code .` meaning, open vscode in your current directory, remember "." means current dir

OR, you can just use the vscode plugin do that stuff

since i don't really know how that plugin works, we move on to documentation with markdown


there are stuff you need to learn with vscode spefically that I don't really want to research myself cuz i dont use vscode:

1. switching your terminal to wsl
2. accessing wsl from vscode
3. plugins for wsl
4. plugins for your languages (linters, real time preview)
5. plugin for markdown preview
6. i cant think of more rn

---

[markdown](markdown.md)
# markdown

i recommend reading why markdown is used for lots of things [markdown: get started](https://www.markdownguide.org/getting-started)

i am writing this documentation in markdown itself, if you are viewing from github, you click on raw
to view the raw markdown

![raw](assets/220805182239.png)

i recommend using the [markdown guide](https://www.markdownguide.org/basic-syntax/) to learn the syntax

to see rendered markdown, you can use a vscode extension

for my usage, i just view the markdown raw in my text editory

> for my usage, i just use vim, a text editor, for most of my stuff, unless an IDE would do better
> this is just my personal use, if you want to learn more do `man vim`, if vim is not installed
> you can do `sudo apt-get install vim`, i do not recommend you do this, unless you work with terminal a lot
> if you are developer, i even recommend you using vscode for most purposes because if the integrations

---

now you can [go](go.md)

# go

using wsl, i recommend you downloading through the command from before

`sudo apt-get install golang`

go through the [documentation](https://go.dev/doc/)

---

once you've gone through the go docs you go to [integration](integration.md)

# integration

now that you've gone through the resources, you are pretty much setup to get you environment setup for development

here are the tools needed for developing

thats pretty much all from me, the takeaway is learn from reading the documentation and how to get the documentation

i highly recommend using the man pages, then asking for help

[linux](linux.md): basic linux navigation and documentation

[git](git.md): source control/looking at diffs (i didnt explain the `diff` command but its pretty cool and its how git works)

[vscode](vscode.md): editing your code, previewing your code

[markdown](markdown.md): for documenting/reading others documentation (how markdown is rendered and created)


## other

man pages i recommend you looking at if you have the time

```
man user
man group

man chown
man chmod

man systemctl
```


i also recommend looking into how servers work, and how they actually host your software,
you don't need to go looking into docker/kubernetes, just basics of how services work

> services work on ubuntu, through systemd (systemd means system daemon), through the interface systemctl (system control)

i recommend learning what are daemons, and what does control mean

> i dont even use systemd on openbsd, haha systemd bloated, rc gang

> if you want to go deepend in your freetime, install linux on ur computer if you want to, maybe linux mint, Pop OS, ubuntu for users who want desktop linux. if you want to just learn how to work with the terminal and learn more about linux, try arch linux and gentoo.

> if you want to go even more deep end, use openbsd (openbsd IS NOT linux or a linux distribution). BSD is its own seperate OS relating to UNIX during the bell labs ATT/ uc berkeley days. may have some similarity, but i repeat IS NOT linux

> even linux has usuablity and has improved a lot for desktop usage, a good competitior to macOS, and Windows for desktop usability allowing for games, creative software, development. (i dont even recommend windows for development unless you are using windows subsystem for linux, macOS is great also for development because it is/was based off BSD/UNIX)

> the only use case for openbsd, is if you want to live/breathe in the terminal, i've excluded a lot since I know developers don't need to know that stuff. I've also excluded a lot of stuff because I don't have the use to explore vscode/ how it integrates with wsl.
