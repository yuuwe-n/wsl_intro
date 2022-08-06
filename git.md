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

this is all you need to know with git, now you can move onto [vscode](vscode.md)

