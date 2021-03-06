Prologue
========

I develop on Windows (yeah, I hear your jeers, linux users!), so to use Git, I use Git for Windows

However, I use Git For Windows (portable version) so I can keep my dev environment centrally located.  This is so I can reuse this environment simply by copying my msysgit directory to a USB drive.

Installation
============

#### (1) Download the latest version of PortableGit:
https://github.com/git-for-windows/git/releases/

You'll want the latest 7z file prefixed with `PortableGit` in the file name.

Extract the 7z file to a directory of your choosing.  For this article, I'll be using `c:\PortableGit\` as a reference point.

#### (2) Ensure PortableGit uses the .bashrc file

`.bashrc` is an important configuration file used by bash to load various custom commands.  Since we are using PortableGit, we need to let it know where to find `.bashrc`.

To do this, add the accompanying `portable.sh` file to the `c:\PortableGit\etc\profile.d\` directory.

This tells PortableGit to load our `.bashrc` file. If you don't have an existing `.bashrc` file, just create an empty one.

#### (3) Setting up your bash environment to use a custom HOME directory

The last step is loading bash and telling it to use a custom `HOME` directory.

1. Create a new directory called `home\portable\` in the folder that you extracted PortableGit to. eg. `c:\PortableGit\home\portable`

2. Next, create a `.bat` in the main `PortableGit` folder to launch bash to use our custom `HOME` directory.

In the following code block, we'll be using [Mintty](https://mintty.github.io/) as our terminal to launch bash since it comes with PortableGit.

The most important part in the `.bat` file is setting our HOME environment variable to use our custom `HOME` directory.

Copy the accompanying `mintty.bat` file to `c:\PortableGit\mintty.bat`.

3. Launch Mintty by double-clicking on `mintty.bat`.

The above example uses Mintty, but you could easily modify the `.bat` file to use some other terminal like ConEmu.
