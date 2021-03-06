# Introduction
This guide was adapted from [r-a-y's](https://github.com/r-a-y/) original blog, available on his Gist.GitHub as of April 2022 (see [`_readme.md`](https://gist.github.com/r-a-y/da6c3b1b99aafcb3e97e311280aa9434)).

I originally posted on reddit asking for suggestions on how to code on my work-environment computers, and the kind folks suggested me to use notepad (no joke). Since I don't have admin privileges on those machines, and I don't particularly love notepad for coding, I started using portable apps until I found out about Portable Git.

Git allows you keep your dev environment centrally located.  This is so we can reuse this environment simply by copying the main directory to a USB drive.

# Installation

## Download the latest version of PortableGit [here](https://github.com/git-for-windows/git/releases/).

You'll want the latest 7z file prefixed with `PortableGit` in the file name.

Extract the 7z file to a directory of your choice.  For this article, I'll be using `c:\PortableGit\` as a reference point.

## Setting up your bash environment to use a custom HOME directory

The last step is loading bash and telling it to use a custom `HOME` directory.

1. Create a new directory called `home\portable\` in the folder that you extracted PortableGit to. eg. `c:\PortableGit\home\portable`

2. Next, create a `.bat` in the main `PortableGit` folder to launch bash to use our custom `HOME` directory.

In the following code block, we'll be using [Mintty](https://mintty.github.io/) as our terminal to launch bash since it comes with PortableGit.
```
set HOME=%~dsp0home/portable
set "MSYSTEM=MINGW64"
start %~dsp0usr/bin/mintty /bin/sh -l
```
The most important part in the `.bat` file is setting our HOME environment variable to use our custom `HOME` directory.

Copy the accompanying `1. mintty.bat` file to `c:\PortableGit\mintty.bat` or write it yourself.

3. Launch Mintty by double-clicking on `1. mintty.bat`.

The above example uses Mintty, but you could easily modify the `.bat` file to use some other terminal emulators like [ConEmu](https://conemu.github.io/).
