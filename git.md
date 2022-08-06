# git

i recommend skimming through the man doc for git
`man git`

in the manual it says to go to for more information
[https://git-scm.com/docs](https://git-scm.com/docs)

once you should at least have a basic understanding of how the source management system git works

here are some commands that you will be making very often however:
```
git clone : clones a repository

git add .
git commit -m "message"
git push
```
for a basic understanding:

```
`git add .` means add the current changes for the '.' current directory, remember that'.' means current directory
`git commit -m "message"` means commit the current changes under a commit called "mesage"
`git push` sends the commit to the git repo,
```

if you want to just do offline edits, you can just do `git add .` and `git commit -m "message`
for local development, these alow you to track changes with these 2 commands

this is all you need to know with git, now you can move onto [vscode](vscode.md)
