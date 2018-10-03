
# Git Command Line Materials
<!-- MarkdownTOC -->

1. [Why Command Line?](#why-command-line)
1. [Quick Reference](#quick-reference)
	1. [General Commands](#general-commands)
	1. [Reading Files \(with Less\)](#reading-files-with-less)
	1. [Editing Files \(with vim\)](#editing-files-with-vim)
	1. [Getting Help with Git](#getting-help-with-git)
	1. [Starting a Repository](#starting-a-repository)
	1. [Adding Files and Committing Changes](#adding-files-and-committing-changes)
	1. [Branches](#branches)
	1. [Showing Recent Work](#showing-recent-work)
	1. [Logging and History](#logging-and-history)
	1. [See Previous Commits](#see-previous-commits)
	1. [Changing History](#changing-history)
	1. [Remotes, clouds and GitHub](#remotes-clouds-and-github)
1. [Things to Learn](#things-to-learn)
	1. [Getting Started](#getting-started)
	1. [Fundamentals of Using the Command Line](#fundamentals-of-using-the-command-line)
		1. [Challenge 1 \(Starting out on the Command Line\)](#challenge-1-starting-out-on-the-command-line)
	1. [Getting Help with Git](#getting-help-with-git-1)
	1. [Starting up Git](#starting-up-git)
	1. [Committing](#committing)
		1. [Challenge 2 \(Starting up Git\)](#challenge-2-starting-up-git)
	1. [The Staging Area](#the-staging-area)
		1. [Challenge 3 \(Committing\)](#challenge-3-committing)
	1. [Seeing your history](#seeing-your-history)
	1. [Searching your history](#searching-your-history)
		1. [Challenge 4 \(See your history\)](#challenge-4-see-your-history)
	1. [Aliases](#aliases)
	1. [Branches](#branches-1)
		1. [Challenge 5 \(Branches\)](#challenge-5-branches)
	1. [Time Travel](#time-travel)
		1. [Challenge 6 \(Moving through your history\)](#challenge-6-moving-through-your-history)
	1. [GitHub and Remotes](#github-and-remotes)
		1. [Challenge 7 \(Remotes\)](#challenge-7-remotes)
1. [Vocabulary](#vocabulary)
1. [General commands \(for UNIX\)](#general-commands-for-unix)
1. [Git commands](#git-commands)
	1. [Help](#help)
	1. [Using the Reader \(called less\)](#using-the-reader-called-less)
	1. [Setting up your git program](#setting-up-your-git-program)
	1. [Ignoring files](#ignoring-files)
	1. [Starting a Git Repository](#starting-a-git-repository)
	1. [Adding files and Committing Changes](#adding-files-and-committing-changes-1)
	1. [Seeing your History](#seeing-your-history-1)
	1. [Advanced History Searching](#advanced-history-searching)
	1. [Using your History](#using-your-history)
		1. [Moving through Time](#moving-through-time)
		1. [Changing History](#changing-history-1)
	1. [Making and Using Branches](#making-and-using-branches)
	1. [Syncing with GitHub](#syncing-with-github)
1. [Sample Files](#sample-files)
	1. [First Sample File](#first-sample-file)
	1. [Second](#second)
1. [Further Resources](#further-resources)
	1. [Additional Command Line Resources](#additional-command-line-resources)
	1. [Recommended Documentation and Materials](#recommended-documentation-and-materials)
	1. [Nice Tutorials](#nice-tutorials)
	1. [More thorough guides](#more-thorough-guides)

<!-- /MarkdownTOC -->

## Why Command Line?
* Default way to use git 
	* helpful for getting help and doing tricky things
* Cloud computing, super computers, Docker will be best used with a command line
* More reliable and consistent (older computers can be used for longer)
* Powerful!


## Quick Reference

### General Commands

Command                | Description
---                    | ---
`man [command]`        | **Manual:**	Read manual or help file for [command]
`ls`                   | **List** files and folders in current folder/directory
`cd [directory]`       | **Change** your current **Directory** to [directory]
`pwd`                  | **Print** the directory that you are currently in (**Working Directory**)
`mkdir [name]`         | **Make** a new folder or **Directory** with name [name]
`cp [file] [copy]`     | **C**o**p**y [file] to [copy]
`mv [file] [new_name]` | **M**o**v**e [file] to [new_name]
`rm [file]`            | **R**e**m**ove [file]. PERMANENT!
`.`                    | Short-cut for current folder
`..`                   | Short-cut for folder above current folder

### Reading Files (with Less)

Command                | Description
---                    | ---
`less [file]`          | read [file]
`h`                    | read help file (once opened Less)
`j`                    | 1 line down
`k`                    | 1 line up
`d`                    | 1/2 window down
`u`                    | 1/2 window up
`G`                    | bottom of file
`g`                    | top of file
`/[text]`              | search for text in file (hit enter to search)
`n`                    | scroll to next hit
`N`                    | scroll to previous hit

### Editing Files (with vim)

Command      | Description
---          | ---
`vim [file]` | edit [file] with vim program
`i`          | Enter "insert" mode.  Now you can type
`esc`        | Escape current mode into "normal mode" where letters are commadns
`:w`         | Save file
`:q`         | Quit

### Getting Help with Git

Command                       | Description
---                           | ---
`git help [command]`          | Read help on the git sub-command [command]
`git help -a`                 | List all available sub-commands
`git help -g`                 | List all available guides / tutorials
`git help glossary`           | Read the built in glossary


### Starting a Repository

Command                       | Description
---                           | ---
`git status`                  | Check current status of current repository
`git init`                    | Start git repository in current folder

### Adding Files and Committing Changes

Command                       | Description
---                           | ---
`git add [file]`              | start tracking the file [file]
`git add [file]`              | add changes to [file] to staging area
`git commit -a -m "mess"`     | commit all changes with message "mess"
`git commit -m "mess"`        | commit all staged changes with message "mess"

### Branches

Command                       | Description
---                           | ---
`git branch`                  | List all branches and current branch
`git branch [name]`           | Make new branch with name [name]
`git checkout [name]`         | Move to branch [name]
`git merge [name]`            | Merge branch [name] into current branch


### Showing Recent Work

Command                       | Description
---                           | ---
`git diff`                    | Shows changes made since last commit
`git diff [file]`             | Shows changes for specific file only
`git diff [SHA] [SHA]`        | Shows differences between any two commits (identified by [SHA])

### Logging and History

Command                             | Description
---                                 | ---
`git log`                           | Shows a log of your commit history
`git log --oneline`                 | Shows abbreviated history
`git log --stat`                    | shows changed files and number of changes
`git log -n X`                      | Log only x most recent commits
`git log [file]`                    | Show only commits that changed [file]
`git log -L [st],[end]:[file]`      | Show only commits that have affected [file] from lines [st] to [end]
`git log --author=[name]`           | Show only commits done by [name]
`git log [--after,--before] [date]` | Log commits or history only before or after the [date] provided.
`git log [-S,-G] [pattern]`         | Show commits that involved a change to [pattern]
`git log --grep [text]`             | Show only commits that have [text] in the message
`git blame [file]`                  | Show last commit to affect each line of [file]


### See Previous Commits

Command                       | Description
---                           | ---
`git checkout [SHA]`          | Change current version to that of commit [SHA]
`git checkout [name]`         | Return to most recent commit of branch [name]


### Changing History

Command                       | Description
---                           | ---
`git checkout HEAD -- [file]` | Discard changes to file and return to most recent commit
`git reset HEAD [file]`       | Unstage changes but keep them in the files
`git revert [SHA]`            | Undo commit [SHA] with new cancelling commit
`git reset [SHA]`             | Reset repository to commit [SHA] (--hard, --mixed, --soft)

### Remotes, clouds and GitHub

Command                       | Description
---                           | ---
`git remote -v`               | List all remotes
`git remote add [name] [URL]` | Add remote at [URL] under name [name]
`git push [name] [branch]`    | Push branch [branch] to remote [name]
`git pull [name] [branch]`    | Pull branch [branch] from remote [name]
`git push -u [name] [branch]` | Push and set remote as upstream for branch (automatically used)
`git clone [URL]`             | Pulls the repo at [URL] to your compute, keeps [URL] as remote

---

---



## Things to Learn

### Getting Started
* Command line app: **Mac:** `Terminal.app`; **Windows:** `GitBASH`.
* Command -> action + output
* Structure of a command: 

`command sub-command -o --option target/argument`

`command sub-command [-o] [--option] [target/argument]`


### Fundamentals of Using the Command Line

* **Help!!:** `man`
* **Moving Around:** `pwd`, `cd`, `ls`, (`mkdir`, `mv`, `cp`, `rm`)
* Editing text: `vim`
	* `i`, `esc`
	* `:w`, `:q`


#### Challenge 1 (Starting out on the Command Line)

* Make a folder for this set of exercises where ever suits you.
* Open your command line.
* Find out which folder it starts in by default
	* Can you use either *pwd* or *ls* to do so?
* Navigate to the folder you've set up for command line git.

**Extension**

* Can you figure out what “.” and “..” represent in the command line?
	* Using `ls` or `cd` will help you.
* after entering the command ‘vim’, can you get back to the command line?
* Can you tell me what the command `ln` does?
* Don’t like the appearance of your command line, especially the prompt?
	* You can customise the look of the prompt.
	* In your home directory ($HOME), create a profile called .bash_profile
	* In that file, add one of the following lines of code:
		* `export PS1="\n(\!)-(\[\e[37m\]\t\[\e[0m\])-(\[\e[31m\]\u\[\e[0m\])-(\[\e[36m\]\w\[\e[0m\])\n> "`
		* `export PS1="\n(\t)-(\w)\n> "`
	* Start a new terminal window … like the change?
* You can also probably edit the general appearance of your command prompt in Terminal or GitBash’s preferences

---

---

### Getting Help with Git
* Google + Stack Overflow
* `git help [command]`
* `less` and navigation

### Starting up Git
* folder - repo - `git init` - `git status`
* `add [file]` - edit - `git diff`

### Committing
* `git commit -am "message"`
* `git log`


#### Challenge 2 (Starting up Git)

* Make sure you are in the folder of your repo for these exercises.
* Initialise your git repository. 
* Create code files by copying from [sample files](#sample-files) below. 
* Add the files to git and commit with a commit message.

**Extension**

* Make a change to the first sample file, and in your commit, omit the -m and message (do only `git commit -a`).  
	* How does git respond?  Can you make it happy?
	* **This is intended to create a potentially unfriendly problem** for you.  It's possible to make it go away, but not intuitive.
* Get familiar with the git help command `git help`
* Figure out how to list all the git subcommands and concepts.

---

---

### The Staging Area

* Working Directory - Staging Area - Repo
* `git commit` v `git commit -a`


#### Challenge 3 (Committing)

* Add the functions of your code file one by one.  
* Commit each one separately, providing a semi-decent commit message.  
* Use the staging area for some of the functions.
* Can you use `git diff` to preview your changes before committing?
* Try changing both of your files, but then only commit changes for one at a time (clue: use the staging area/index)

**Extension**

* review your history with `git log`. Use git help to see what modifications you can make to the way the log is displayed.
* See if you can work out how to use `git add -p`.  
	* Make some changes to a few lines of your file, just for the sake of this extension.  Before staging or committing, run `git add -p`.
* Make some changes to both files, stage one of the files, and find the difference between `git diff` and `git diff --cached`
* What does `git commit --amend` do?

---

---


### Seeing your history
* `git log [--oneline, --stat, [file]]`
* `git show [SHA]`
* `git blame [file]`
* `git diff [--stat] [SHA] [SHA] [file]`


### Searching your history
* `git log [-n, --after, --before, --author]`
* `git log [--grep, -G, -L]`


#### Challenge 4 (See your history)

* Given commands for logging, and what you know about your history
	* Experiment with the log command however you like, OR ...
	* Use `-n` to show only the last two commits
	* Use `--before` to isolate the first commit
	* Use `--grep` to get only your first commit
	* Use `-S` to get only the commits in which you changed the function "division"
	* Use `-L` to specify the lines for a specific function in the code


---

---

### Aliases
* `git config --global alias.quick_commit "commit -a -m "whatever, get it done!"`
* `git config --global alias.qlg "log --oneline --stat"`


### Branches
* `git branch [-v]`
* `git branch [name]`
* `git checkout [name]`
* `git merge [other_branch]`

#### Challenge 5 (Branches)
* While doing this challenge, try to check your status log and your file constantly to see the changes `checkout [branch name]` and `git merge` are making to your files.

* Make a new branch
	* In the new branch, create a new function (with copy and paste if you like).
	* Add and/or commit as usual.
	* Merge the new branch back into the master branch.

* Make a new branch.  
	* Change a function in the master branch, and commit that change.  
	* Now change the same function in the new branch, but in a different way.  
	* Try merging the new branch into the master branch.
	* Can you fix the problem?


---

---

### Time Travel
* `git checkout [SHA]`
	* `git branch [split branch]`
* `git checkout [branchName]`
* `git revert [SHA]`
* `git reset [--soft, --mixed, --hard][SHA]`



#### Challenge 6 (Moving through your history)


* Revert your last commit 
* Revert that reversion
* Reset your repo to before you bothered with the reversions (careful with reset)
* Look at what your main code file looked like after your second commit. THen return to the present

* Delete a file and bring it back


**Extension**

* There are three modes of resetting: soft, mixed and hard.  Try to work out the differences between them by experimentation.
* When you have travelled back in time and checked out another commit, try to make some changes and commit them.  
	* What happens?  What happens if you go back to the "present" with `git checkout master`? 

---

---


### GitHub and Remotes
* `git remote add [name] [URL]`
* `git push\pull [remote] [branch]`
* `git clone [URL]`

#### Challenge 7 (Remotes)

* Clone the repo for this document with the URL `https://github.com/maegul/command_line_materials.git`

`git clone [URL]`
`git clone https://github.com/maegul/command_line_materials.git`

* Check to see the files are on your computer
* Create an empty repo on your github account ...
	* copy the URL to it 
	* Add it as a remote to your new local repository
	* push this document to your own github repo

---

---

## Vocabulary

**Less**

Program for reading files in the command line.  A "Reader".

**Vim**

Program for editing text in the command line.  Popular text editor.

**Repository**

A folder where git is keeping track of all the changes you make to all the files in it.
All the changes are recorded as commits, which git keeps as a log or diary of changes.
Additionally, there may be parallel versions or copies too, known as branches. 

*All this, the records and information that git keeps to track your changes and versions, as well as the actual contents of the folder, is a repository*

**Commit**

How you put something in your diary or history - a single diary entry.
All changes since the last commit are recorded, or "committed", and become a specific version or "commit".

As a noun, it refers to a set of changes recorded as a particular version of your repository.
As a verb, it refers to the act of recording these changes

**Working Directory + Staging Area**

The *Working Directory* is simply your files, as you've known them before git.  
This is simply the files on your hard drive before git gets involved and whether you've committed them or not.  
If you save some changes to your file, you've changed the working directory.

The *Staging Area* is a temporary storage area for changes you've made since your last commit.  
Before committing certain changes, you can store them in the staging area.
This is useful for when you only want to commit a small amount of the changes you've made at a time, into separate commits.
It's a way of sorting many changes into related groups, so that your history makes more sense.
It is not necessary to use it.
Many users of git often skip using it.

**Log**

A list of your commits, generally listed in chronological order.

**Branch**
A history of commits that is parallel to other history of commits.
Two branches will have 

**Master**

The name for the default branch, or set of versions, or timeline of changes.
Mostly relevant only when you have multiple timelines or universes.

**Branch**

A Parallel Universe of versions and history.
Branches are split from a common commit, and can be put back together through *merging*.
Otherwise, they are independent versions that do not affect each other and which can be accessed separately.


**Merge**

Put history of one branch into another so that the changes made in that branch have now been made in the current branch.
This doesn't make the two branches identical.
It is a one way operation.
It simply applies the changes of one branch onto the current branch.

**Hunk**

A particular region or location in your file where Git has detected changes.


**Remote**

Another computer, typically a cloud service, that will store git repositories accessible over the internet or a network.
As with merging branches, you merge your remote repositories with your local repositories (the ones on your computer).
This is done, typically, with the `push` and `pull` commands.

**Origin**

As with "master", the default name of the remote for a repository.

**HEAD**
Is a reference to the last commit in the currently checked-out branch.
The "head" of your branch, in a way.





## General commands (for UNIX)

**Help or Manual**

> man [command]

Open up the manual or help file for [command], using the "reader" app called `less`.

Consider installing and using the app [tldr](https://tldr.sh) for quick and practical help.

**List**

> ls 

Lists the contents of the current directory.

A number of useful options are:
* `la -a` - list all, including hidden files
* `ls -l` - list many details about files
* `ls -Fhalt` - typical set of options.

**Change Directory**

> cd [directory]

_Change to specified directory_

> cd ..

_Change to the directory above.  The double dots means 'directory above'_

The command `cd` without any argument moves you to your HOME directory.
If you want to know what directory this is, enter `echo $HOME` into your command prompt.

Often, important files are stored directly in your HOME directory.


**Where am I**

> pwd

_Print working directory ... the directory we are in now._


**Make A New Directory**

> mkdir [new directory name]

_Make a new directory in the directory that you are currently in._


**Copy**

> cp [original file] [new file]

_Copy the original file to a file named what you specify in "new file"_
_File specifications can include whole directories too: "/my_folder/file.txt"_

**Move**

> mv [original file] [new file]

_Much like cp, but doesn't copy the file into a new one, just moves it._

Can be used to rename files.


**Remove or Delete**
> rm [file]
> rm -r [directory]

_Remove (or delete) a file or directory._
_This is permanent!_
_Using the "-r" flag is necessary for directories_




## Git commands

### Help

**General Help**

> git help

**Help for specific command**

> git help [command]

> git help commit

Like with `man` above, brings up the help file for the specific git sub-command.

**Look up General Help**

> git help -a

*list all subcommands.  Useful for when you can't quite remember which command you want to use.*

> git help -g

*list general guides including a tutorial and suggested workflows*

> git help glossary

*Search for a term by pressing "/" then your word, and enter.  Go to each find with "n" or "N" to go backwards.  See Using the Reader (less) for more.*

### Using the Reader (called less)

The above help commands automatically use a reading app for the terminal called `less`.
This is useful because you aren't dumping the whole file into the output of your command line app.
Instead, you can view the file, and when done, quite `less`, and make the whole file disappear.
To navigate and search the file you've just opened, the following commands will be helpful.


**Getting Help**

key or command | action
---            | ---
h              | read help file

**Moving around**

key or command | action
---            | ---
j              | 1 line down
k              | 1 line up
d              | 1/2 window down
u              | 1/2 window up
G              | bottom of file
g              | top of file

**Searching**

key or command | action
---            | ---
/[text]        | search for text in file (hit enter to search)
n              | scroll to next hit
N              | scroll to previous hit


### Setting up your git program

The behaviour of git can be configured.
This configuration can apply to everytime you use git anywhere on your computer.
Or, it can apply only to when you use git for a particular repository.

In either case, the settings are stored in a file, and the location of that file determines whether it applies everywhere on your computer or just for a particular repository.

**Global Configuration**, which applies everywhere, is stored in the file `$HOME/.gitconfig`.

**Local Configuration**, which applies only to a particular repository, is stored in the repository itself, in the hidden sub-folder: `repository/.git/config`.

To edit these settings, you can either edit these files directly (which may require you creating the files first), **or, you can use the following commands to have git edit the files for you.**

All the settings dealt with below typically apply to your whole computer and not to a particular repository.  Thus the use of the `--global` option.  But the syntax is still relevant to repository specific configuration.


**Configure your user name**
> git config --global user.name [My Name] 

_Lets git know who you are_
_If you ever collaborate with others, this way people can know which commits are yours._

**Configure your email**

> git config --global user.email my.email@myEmailProvider.com 

_Tell Git your email address_
_Create a config file in your home directory_


**Change default text editor**

[Quick Guide](https://help.github.com/articles/associating-text-editors-with-git/)

> git config --global core.editor "atom --wait"

**Add Aliases**

Aliases are sub-commands of your own making which run a custom, and often long, git command that you define.

Useful for making short versions of common commands, or for saving long complicated commands on speed dial for quick recall.

> git config --global alias.quick_commit "commit -a -m "whatever, get it done!"

Now, `git quick_commit` will run the above command.

*Notice the lack of a git in the quotation marks*

Some aliases you may find useful:
* `alias.lg "log --pretty=format:'%C(yellow)%h %Cred%ad %Cblue%an%Cgreen%d %Creset%s' --date=short"`
* `alias.lga "log --pretty=format:'%C(yellow)%h %Cred%ad %Cblue%an%Cgreen%d %Creset%s' --date=short --all --graph"`
* `alias.aliases config --global --get-regexp alias`

**Listing All Configuration Options**

> git config --global -l

**Editing Config File**

> git config --global -e

**An Alias for listing all aliases**

> git config --global alias.alias "config --global --get-regexp alias"


### Ignoring files

Often there are files that you don't want git to pay attention to.

This [quick guide by GitHub](https://help.github.com/articles/ignoring-files/) is helpful on this topic.

**Ignore particular files in your repository**

* Add to your repository the file `.gitignore` (the dot is important).
* For each file you wish to ignore, at its name on a new blank line.
* Patterns that use wild cards `*` can be used to ignore groups of files with similarities in their file names, like `*.pyc`.

**Ignore files everywhere you use git on your computer**

* You can create a file just like the `.gitignore` file above, and place it in your `$HOME` directory.
* Once you've done this, use the command below to tell git which file to use for a *global ignore file*, and then it will be applied all over your computer.

> git config --global core.excludesfile [directory and name of your ignore file]




### Starting a Git Repository

> git init 

_Create that hidden .git directory so Git is ready to start working with your project._


> git status 

_“Hey Git, what’s up right now?”_
_Displays general information about your current repository._


### Adding files and Committing Changes
_Your Captain's Log or Diary_

**Add a File**

> git add [file] 

_Tell git to now keep records on a file so you can commit changes you've made to it._

Alternatively, this will stage changes to the file, if you have already been tracking it with git and have previously committed changes to the file with git.

**Commit a Change**

> git commit -m “Commit message here” 

_Whatever changes you've made (and added to the staging area), commit them with the note or message provided after the "-m" flag._

Note that this only commits changes that have been staged.


**Commit ALL Changes without adding to the Staging Area**

> git commit -a -m 'Added first verse' 

_The "-a" flag means: git-add, then do commit_

This means you don't have to worry about staging.

_However, it only works for changes to files that have previously been added.  If you want to commit changes to a new file, you have to add as above, then you can use the above._


### Seeing your History

Some of the commands below are good candidates for turning into aliases.

**See the log**

> git log

_shows captain’s log activity_


> git log --oneline 

_Show the git log in a more concise form._


**Seeing Differences between changes or commits**

> git diff

_Shows differences between current uncommitted changes and those of the most recent commit_


> git diff [path]

_Shows differences only for file specified by path_


>git diff [commit] [commit]

_Shows differences between two specified locations in your history (including branches etc)_


>git diff --word-diff


_Show differences in terms of changes words, not changed lines_


### Advanced History Searching

> git log --stat

> git log --shortstat

> git log --numstat

*numbers on what changes have been made*



> git blame [path]

*Shows only the commits that affect the file defined by path*

> git log -n x

*limit the number of commits you see from your history to x*

> git log [--after | --before] <date>

* Date specifications can look like:
	* 'YYYY-MM-DD HH:MM::SS +1000'
	* 'YYYY-MM-DD'
	* '7 years 5 months 3 days 2 hours ago'

*Specify a time period of your history to look at*

> git log --grep [pattern]

*pattern is in the message for the commit*

> git log -S [pattern]

*pattern has been added or deleted (in change log) in actual text*

> git log -G [pattern]

*Pattern occurs in change log in actual text*

> git log -L [start],[end]:file

*Shows commits that affected the specified line range of the specified file (with respect to present file line numbers)*

> git log --diff-filter [A,D,M, ...]

*See commits that affected files in a particular way (ie, added a file, modified, deleted, etc)*


### Using your History
_Time Travel_

#### Moving through Time

**Going back in time to a previous commit**

> git checkout [unique change id]

_Goes back to the state of your files at this commit_
_Lets you look at your files as they were at this time, and run code if you need to_


**Going back to the present**

> git checkout master

*Here, master is referring to the branch name.  If on another, you need to specify that branch*

#### Changing History

**Cancelling previous commits**

> git revert [unique change id]

_The "Unique Change ID" is what the commands "git log" give you for each commit_
_Cancels the changes made in a particular commit, and adds a new commit recording this reversal of changes_

**Undoing Work before its committed**

> git checkout HEAD -- [file]

*Any changes not committed will be discarded*


**Re-Writing History**

> git revert SHA

> git reset SHA

* soft (kind of default)
* hard
* all with possibility of specifying path


### Making and Using Branches
_Parallel Universes_

**List all Current Branches**
> git branch

**Make a new Branch**
> git branch [branch name]

**Go to a branch**
> git checkout [branch name]


**Merge the History of a branch into the current branch**
> git merge [branch name]

_Takes the history of "branch name" and merges that into the branch you are current in._
_Running "git branch" before, to confirm which branch you're in maybe helpful._
_If there are different changes in each branch that can't be merged, ie that conflict with each other, you will get a conflict that needs to be resolved._


### Syncing with GitHub
_Sharing your repositories online_

**List current Remotes**
> git remote -v

**Add your GitHub (or other) repository to your local repository**

> git remote add [name] [URL]

_Adds the URL of your online Repo to your local repo under the name you provide._
_Within Git, this is the name of the remote that you are using_


**Put your Local History onto your Online Repo**
> git push [remote name] [branch]

_Takes all of the history of the branch you specify and adds it to the remote you specify_
_This history is put into a branch of the same name as your local one, the one you specify._


**Bring changes that are on your online repo into your local Repo**

> git pull [remote name] [branch]

_Here, "branch" specifies the branch name in the GitHub account (which will generally be the same name as the one on your local computer, as it will have been created by you doing "git push" as above)_

_Will take the history of the "branch" on "remote name" and merge it into the branch you are currently in_
	

**Clone a Remote Repo**

> git clone [URL]

Where [URL] points to an online repository, on GitHub lets say.

That online repository will be pulled down into a whole new repository on your computer, in a new folder too.
* You will have control over the local repository.
* The remote of this repository will be the one you've clones.
* Usually, you will not have control over the remote, so you will not be able to `push` but you will be able to `pull` changes.
* If necessary, you will be able to add an additional remote, one that you control, so that you can push changes to a remote repository.


## Sample Files

* These files are simple python scripts.
* All the code has been commented out with `#` symbols.  This is so that you don't have to type anything, but simply uncomment code.
	* Usually, there will be a hot-key for you text editor that does this for you.

### First Sample File

```python
# def addition(a, b):

# 	summation = a + b

# 	return summation


# def subtraction(a, b):

# 	difference = a - b

# 	return difference


# def division(a, b):

# 	quotient = a / b

# 	return quotient

# def multiplication(a, b):

# 	product = a * b

# 	return product
```

### Second

```python
# def bad_addition(a, b):

# 	summation = a + b + 0.002

# 	return summation


# def bad_subtraction(a, b):

# 	difference = a - b + 7

# 	return difference


# def bad_division(a, b):

# 	quotient = (a+13) / b

# 	return quotient


# def bad_multiplication(a, b):

# 	product = a * b + 12

# 	return product
```


## Further Resources

### Additional Command Line Resources

* [Command Line Tool for using GitHub from the command line](https://github.com/github/hub)

* [Tool for showing your git status in your prompt](https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh)

### Recommended Documentation and Materials

* [Software Carpentry Course Materials on using git](https://swcarpentry.github.io/git-novice/)

* [Official Guide Book](https://git-scm.com/book/en/v2)


### Nice Tutorials

* [git - the simple guide](http://rogerdudler.github.io/git-guide/)

* [learn enough git to be dangerous](https://www.learnenough.com/git-tutorial#sec-viewing_the_diff)

* [Interactive Tutorial App](https://github.com/jlord/git-it-electron#what-to-install)

* [Interactive Tutorial Web Page](https://learngitbranching.js.org)

### More thorough guides

* [interactive cheat sheet](http://www.ndpsoftware.com/git-cheatsheet.html)

* [git magic](http://www-cs-students.stanford.edu/%7Eblynn/gitmagic/)

* [A visual git reference](http://marklodato.github.io/visual-git-guide/index-en.html)

* [conversational git](http://blog.anvard.org/conversational-git/)

**Quick Link to This Document:** http://go.unimelb.edu.au/etc6