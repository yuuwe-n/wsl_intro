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
