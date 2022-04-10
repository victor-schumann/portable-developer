# Git Cheat Sheet
## Main Commands
First of all, navigate to the repository folder using your preferred terminal; a "repo" is what we call a collection of all the changes you’ve made to your project over time.

To start, let us register your Git data into the repository. Just copy and paste the following commands:

```
git config --global user.name "<your-username-here>"
git config --global user.email "<your-email@here.mail>"
git config --global init.defaultBranch main
git config --global color.ui auto
```
Remember to exclude the '<>'  when you type your own info over there. This peice of code adds an identification to the git repo, changes teh default branch to "main", and set the automatic color scheme.

## SSH Keys
This section will guide you through setting up an SSH key to help you edit your repositories with security. Go to your terminal and type this:

```
ssh-keygen -t ed25519 -C <youremail-here@mail.mail>
cat ~/.ssh/id_ed25519.pub
```
You should see a long string of characters. That is your SSH key! Now copy that, head over to your GitHub account config section and add it.

## Checks
The following code helps you check if everything is up and running. Try it yourself:

```
git config --get user.name
git config --get user.email
git --version
```

## Cloning & Editing

```
git clone <add-your-SSH-URL-here>
```
This command clones a repository. To do so, go to yout GitHub repo of choice, copy the HTTP or the SSH link (click on the green "code" button), and then type this into your terminal, inside the folder of choice. You can also start a whole new repo with the following piece of code:

```
git init
```

## Sync
Probably the most important part of this guide - or at least the most frequent one you are going to reference. First, this is how you get the status of the git repo:

```
git status
```

This bunch does this, respectively:
- Adds the edited files to the staging area;
- Commits the changes with a message of your choice (check the etiquette links on README.md);
- Shows the log of changes on the current session;
- Pushes the changes to the git cloud. 

```
git add <your-edited-files-go-here>
git commit -m "Insert the message you want to be displayed here
git log
git push
```

P.S.: Whenever you want to sync it all FROM git, use the command PULL instead of PUSH.

P.P.S.: The message, “Your branch is ahead of ‘origin/main’ by 1 commit” just means that you now have newer snapshots than what is on your remote repository. You can upload them with the GIT PUSH command. If you get any more errors, do not worry. Part of the journey is to learn how to fix stuff!

# Cheat Codes Index
- `git init` creates a .git repository in your project;
- When using `git add <filename.ext>`, replace <filename.ext> to a file you are trying to add like “index.html”. This will add the file to what is called a “staging area” or index. Think of the staging area like a section where things are getting set up to be moved to your repository. To add everything to that area, replace <filename.ext> with a simple dot (.). Alternatively, if you want to add every file that ends with md, for example, replace it with `*.md`.
- `git status` shows what has already been added to the staging area and what files have been changed that need to be added to the staging area.
- `git reset filename.extension` removes specified file from the staging area.
- `touch .gitignore` creates an editable text file that lists folders or files that you do not want to be involved in any changes along the life of the project.
- `git branch branchName` creates what we call a branch - direct copy of your code from another branch.
- `git merge branchName` takes the commits from the branch you were working on and merge them together with main.
- `git remote add origin https://github.com/userName/project.git` adds the local files to the location of your remote repository.
- `git push -u origin master` "pushes" your local repository to your remote repository. This command only needs to be written like this when you do it for the first time.
- `git push` sends your code to GitHub after your initial push.
- `git clone https://github.com/userName/project.git` allows you to clone (or download) the entire project into the directory you are working.
- `git pull` allows you to pull the latest version from the remote repository and update your local version so you can work with the latest updates as their changes enter the codebase.
