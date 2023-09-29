# Sharing Git

## Description of Git

Git is the same program like Zoom, MS Office etc.

We will know:

* What is Git and it profits
* Why command line 
* How to transfer in file system
* How to execute clue commands with files and folders: copying, moving, creating, deleting, reading
* How to install Git and adjust it 

> [!NOTE]
> Learning of command line helps to understand Git installing process and use more it opportunities.

## What is Git

It is VCS (Version Control System) or SCM (Source Control Management).

Also Git helps work in team.

# Installing of command line for Windows users.

> [! NOTE]
> If you are Linux or MacOS user you have command line already.

In daily work most user use commands with use in MacOS and Linux. For Windows for it we need install Git bash.

There is Oficial Git for Windows on [website](https://git-scm.com/download/win "git-scm.com").

1. Go to oficial website written abow.
2. Download one of **Standalone installer**, version that you need.
3. Run installer and notice where it be insalled, casually it is `C:\Program Files\Git`
4. Check if choosed **Git Bash Here**, it gives you ability to open console bash in any folder.
5. Further if possible stay in default settings and press `Next`
6. After accomplishment press **Finish**

## First run of Git Bash

It possible do from search bar of it can do by open `C:\Program Files\Git\bin`

It will writen the same.

```bash
USER_NAME@HOST_NAME MINGW64 ~
```

Hurra!!! We have installed Git!

# Meet of comand line

Graphic User Interface(GUI) shows casual user interface for us. Command line (console, terminal) - also interface just text. It is usually program on your computer.

## Command line and Git.

Git is program wich can work from console. Any graphic interface for Git just convert clicks of mouse to program invoke.

If you have learned to work with terminal, it easier to educate to use graphic shell.

## Fist steps

It's time to work in command line. Start with launch a program.

If you are Linux or MacOS user launch **Terminal**.

It possible do with window OS. Or use a hot keys `Ctrl + Alt + T` for Linux.
And `Cmd + Space` for MacOS and next enter `terminal`

In opened window you will see:

* Your computer name
* Login
* `$` symbol, that signal of command waiting yours commands.

Order of elements could be changed according operational syslem.

**OS Windows and Linux**

```bash
userName@ComputerName ~
```

**MacOS**

```bash
computerName:~userName$
```

## How don't loose oneself

In command line you are in some folder always like in GUI. To know where are you possible by print `pwd` (print working directory).

> [!NOTE]
> **File system is not easy**
> Operational system Windows, MacOS and Linux are different. Even file systems.
> Way in Windows commence with disk letter C `/c/` or `c:/`. No letters in Linux,
 but home directory stay in `/home` instead `/Users`. In MacOS there is `/Users` folder but 
 no letters. 
 
 To transfer folder press `cd` (change directory).
 
 For go to home directory press `cd ~`
 
 # Command line navigation
 
Output contain of directory `ls`
 
Change directory `cd folderName`

If you're stay `/projects` enter `cd github` it transfer you to `/projects/github`.

To come back in parent direcory (upper level) press `..` instead folder name.

To call temporary directory press `.`. It necessary in case scripts, with input 
forder like parameter.

To transfer through several directory we must diverse forders wich we visit 
during path with `/`.

## Additional opportunities `ls`

Many commands have additional options. Exempli gratia if  you call 
`ls` you see common file list. But if call `ls` with flag `-a`you output extended list.
It shows all hiden files wich starts with `.` e.g. configuration files. And two peculiar 
files `.` and `..` wich signs temporary and parent folder.

More `ls` can work with home directory symbol (`~`) and previeous directory (`..`).

# Folder and files operations: creating, copiing, moving.

## Creating files and directory - `touch` and `mkdir`

To create file we need enter `touch %fileName%` into consele.

```bash
$ touch ny-new-file.txt
```

Good practice is to give extension to files to detect substitutional program for
operational system.

To creating directory press `mkdir %directoryName%`.

You can create whole structure by one command using flag `-p`.

`touch` and `mkdir` creating files and folders in temporary directory default. 
But you can determinate directory by home directory character `~` and `/` and further 
directories or relative way by using `..`.

## Copiing files - `cp`

Command `cp` (copy) takes two parameters `what copy` and `where copy`.

```bash
$ cp what_copy where_copy

$ cp index.html src/

#have copied index.html to src folder
```

You can select right several files. 

```bash 
$ cp what_copy what_copy what_copy where_copy
```

## Transfering of files and folders 

There is exist command `mv` - move.

Syntaxis is analogue of `cp`. Commence with command name after files and folders names and 
the end folder where we move. 

# Filse and folders operations: reading and removing

## Reading files - `cat`

To read file enter `cat %fileName%`

## Files and folders removing -`rm`, `rmdir` , `rm -r`

To delete file press `rm %fileName%`. `rm` - remove.

Delete directory you can with command `rmdir`.

If folder not empty you get error `Folder not empty` - it is protection of 
occasional deleting files. 

If you really want delete this folder with files and others folders press `rm -r`
(`-r` - recursive). It remove files and folders consistently and the end delete necessary directory.

# Effective work with command line

## Execute rigth several commands by `&&`

Between commands use double ampersend and you execute commands consistently.

## Invoke commands from buffer

By press up key and down key you can moving between previous commands.

## Use autofilling

Start type command and press `Tab`. If there are many commands start with that letters
terminal shows you commands list. If one command upwrites full command.

Type folder name and tap double `Tab` and console shows you folder containing. 

If list is very long terminal suppose you output all items. Confirm 
action by `y` or decline by `n`.

# Git installing 

## Windows

If you Windows user you have Git already. Assure with it by executing next command:
```bash 
$ git version
```
Console output temporary version, if all alright.

## MacOS

Thre are two ways to install Git.
 
**First.**  Open console and execute command `usr/bin/git`. Installer will run.
Press **install**.

**Second.** Use **Homebrew**

1. Install package manager
* Go to [Official Homebrew site](https://brew.sh/ "Homebrew manager")
* Press it to copy
* Find program Terminal, paste copied text and press `Enter`.
2. Install Git

```bash
$ brew install git
```

## Linux

* Go to [Official Git site] (https://git-scm.com/download/linux "Git"). 
* Coose installing command for your version Linux.
* Copy command and paste to Terminal.

## To check if all right

Enter next command:

```bash
$ git version
```

If all right there is showing Git version.

# Adjusting Git

## Work with adjusting file `.gitconfig`

If you work in command you must present yourself. You can grant any name and any email.
To do it possible with command `git config` (configuration) with key `--global`. 
`git config --global` will work anywhere, any folder. 

`user.name` - we need indicate our nikname or name. `user.email` - our email.

Git reserve all global settings in the file `.gitconfig` in home directory. 
You can read file `.gitconfig` by

```bash
$ cat ~/.gitconfig
```

Or by `--list`
```bash
$ git config --list
```

# Initialize repository

## Make folder with repository `git init`

Open folder with necessary repository by `cd` and enter:
```bash
$ git init
```

> [!NOTE] Commence branch
> Commence branch could be call or `master` or `main`, dependent of version Git.

Git create in your folder repository `.git` (`%yourFolder%/.git`)

## UnGit folder if something wrong `rm -rf .git`

For ungit repository you need delete secret folder `.git`.

Key `-r` - recursive, allow delete folders with their containing.

Key `-f` - force, rid you from questions like `Do you really want delete this file? And this?`

> [!CAUTION]
> In subfolder `.git` store editing history of project. You could not restore previous data.
Remains later files version only.

## Check consistention of repository - `git status`

Command `git status` output:

* `On branch master` or `On brach main`
* `No commits yet`
* Message to commit something you need to create at start by `git add`

## Preparing files to saving - `git add`

To prepare to saving files you can by :

```bash 
$ git add %fileName% # preparing one file or several
$ git add --all # preparing all files in directory 
$ git add . # preparing temporary folder
```

> [!NOTE]
> Adding files is not a commit. This don't saving a file version.

# Commit 

## Make commit - `git commit` 

Make commit with message `-m`. In message you clarify what changes in commit were. 

```bash
$ git commit -m 'Commit message'
```

# Look commits history 

## `git log`

Attend that `git log` output commits in reversed chronological order default. 
Later commits shows on the top.

# GitHub 

You can create public, private and team repository on GitHub. GitHub is remote repository.

# GitHub sign up

Go to [GitHub](https://github.com/) and sign up.

# Creating remote repository.

1. Go to in your profile by link `https://github.com/username`
2. Create repository. Go to tab **Repositories** and press green button **New**.
3. Entitle repository. This name could distinguish from repository on your computer.
And press **Create repository**

# SSH Keys. 

SSH key assure your personality and rights on read and editing files. 

SSH (Secure Shell Protocol). It encrypt traffic. 

SSH use couple keys
* **private** your personal key. With this key you can decrypt files for you. 
* **public** - accessing for all. With puclic key anyone can encrypt files for you.

## Checking existance SSH-key.

Default place of SSH-key is home direcory. Go to it.

```bash 
$ cd ~
```

Check existance of SSH key wich stay in `.ssh/`
```bash
ls  -la .ssh/
```

If folder empty you can create new SSH keys.

## Generating SSH key

1. For generating SSH-couple you can use program `ssh-keygen`

```bash 
$ ssh-keygen -t ed25519 -C "%yourEmail%"
```

If there is error use another algorythm

```bash
$ ssh-keygen -t rsa -b 4096 -C "%yourEmail%"
```

2. Sign key place storage. You can use place default. Just press `Enter`.
3. Program will ask passphrase for access SSH-key. You can stay empty. Press `Enter`.
And to confirm press `Enter`.
4. Done! Check!
```bash
ls -a ~/.ssh
```
There are one file with extension `.pub` and without. `.pub` - public key. Without private.

# Bind SSH-key to GitHub

1. You need copy public ssh key

**MacOS**
```bash
$ pbcopy < ~.shh/id_rsa.pub
# for ed25519
$ pbcopy < ~.shh/id_ed25519.pub
```

`pbcopy` copy stream of data.

Alternative way to print contain by `cat`, and copy manual.

**Windows**
```bash
$ clip < ~/.shh/id_rsa.pub
# or 
$ clip < ~/.shh/id_ed25519.pub
```

or use `cat`

2. Go to GitHub **Settings** in account menu. 
3. In left menu press **SHH and GPG keys**
4. In new tap press **New SSH key**
5. Into field **Title** enter name of key e.g. **Personal key**
6. In field **Key type** must be **Authentication**
7. In field Key paste your key from buffer.
8. Press **Add SSH key**
9. Assure key.
```bash
$ ssh -T git@github.com
```
There is warning about first connection. 

Check SSH key of GitHub by [link](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/githubs-ssh-key-fingerprints "GitHub Keys").
If OK enter `yes`. And you see welcome.

# Bind local and remote repository

## Bind remote repository to local `git remote add`

Go to page of remote repository, choose type `SSH` and copy URL.

Open console goto local repository and enter commadn `git remote add`

```bash 
$ cd %localRepository%
$ git remote add origin git@github.com:%accountName%/%remoteRepository%.git
```

To command necessary give two parameters: name of remote repository and it URL.

> [!NOTE] 
> To paste in command line in Git Bash and Linux press matched keys `Ctrl+Shift+V`,
on MacOS `Cmd+V`.

`origin` - standart pseudonym with it we can call main remote repository. Usually it is one.
It make easy work.

## Assure that repositories bind - `git remote -v`

Flag `-v` shortcut of `--verbose`.

# Syncronizing local and remote repositories

Commits stores in branches. First branch is `main` or `master`.

## Send to remote repository - `git push`

First time this command we need call with flag `-u` and parameter `origin` and
name of temporary branch `main` or `master`.

```bash 
$ git push -u origin main # if error press master instead main
```

## GUI GitHub

Press **commit** to show all commits of repository.

# File README.md

To understand what project it is we describin it in `README.md`

## Why README.md

1. Name of project end short description
2. Technologies used in project and what difference of another
3. Project documentation - comprehensive information, what is project.
4. Project plans if there are.

## README.md execution

You can decorate your file by language `markdown`.

There is instructions [markdown syntaxis](https://docs.github.com/ru/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

# Researching log 

Log consist with hash (unic code), Author, Date and commit message.

Short commits list we can get by `git log --oneline'

Short cashe is unic too for this set.

> [!NOTE] 
> If you don't way out from commits log press `Q` (quit).

`HEAD` indicate the last commit. `HEAD` - is file wich stores in service folder `.git`.

You can sign `HEAD` instead hash of last commit.

## Statuses 

* `untracked` Git don't observe this file but see
* `staged` - prepared file

> [!NOTE]
> Staging files sometime call `indexed` or `cached`.

* `tracked` - opposite `untracked`. Commited and added files.
* `modified`

## `staged` and `modified` 

`git add` makes temporary consistence only. If add file and then edit. Later consistence won't refreshed.

For refresh press `git add` again.

# Messages decoration of commits 

When output `git log --oneline` message placed during 72 symbols. 
A lot of rules include item: "Message mustn't be bigger 72 symbols".

## Message must be informative

* Message must be sufficient short to easy read
* Must be informative 

## Decoration styles 

It could be used imperative verbs, past verbs or nouns.

## Corporative rules 

A lot of companies use Jira - organization system of project and tasks. Every task have identificator.
Writes identificator e.g. project and task number. `LGS-239` **LGS** (Logistic) and task 
number 239.

## Conventional Commits 

Format is `<type>:<message>`.

Type could be:
* feat
* fix 

You can visil [linl](https://www.conventionalcommits.org/ru/v1.0.0-beta.4/#спецификация "Conventional commits") 
to see description of rules.

## GitHub - style 

You can indicate link to task by `#<taskNumber>`. 

This way GitHub bind commit and task.

> [!NOTE] 
> For messages on Russian reccomends use infinitives. `Добавить тесты для Pipka Service`,
`Исправить ошибку #123`.

> For messages on English recommends use imperative. E.g.: `Use library mega_lib_300`,
`Fix exit button` etc.

> This recomendation became hisorical, and many projects implicate that.

# Diagrams Mermaid 

Visit [link](https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/ "Mermaid")
with mermaid description. It is diagram code. 

# How to fix commit 

`git commit --amend`

> [!NOTE]
> Option `--amend` works with last commit only.

## Assume commit new files `git commit --amend --no-edit`

```bash
git add newFile.txt
git commit --amend --no-edit
```

## Edit commit message - `git commit --amend -m "New message".

## If editor opened

* nano: Editing the top string and then press `Ctrl+X`( E**x**it)

> [!NOTE] 
> In letters like `^X`, `^G`. This symbol `^` means `Ctrl`.

After exit nano suppose to save, press `y`.

After editor suppose edit file name, but it is not necessary. Press `Enter`.

* Vim: if you can not use Vim - exit and use flag `-m` for sign commit message.

1. Press `Esc`.
2. Type sequence `:qu!`.
3. Press `Enter`.

# How to roll back 

## Do unstage of changes - `git restore --staged <file>`

## Roll back commit - `git reset --hard <commit hash>`

Hash you can find in history.

Be careful you can delete something you need.

## Roll back changes wich don't get to commit or staging -`git restore <file>`

You change file and now it have view `modified`. To reverse press `git restore <file>`.

# Researching of changes in files 

Often it necessary to know what changed difinitelly after determinate commit.

Situations example: 

* You want to do commit but want check if changes get to it. 
* Yesterday your collegue made a commit with a message `small fix`, after
tests of project get fault. To reason in situation need to look changes.

This allow by command `git diff`.

To look changes in `staged` we need use flag `--staged`: `git diff --staged`.

`---a/%fileName%` - old file `+++b/%fileNeme` - new file.

`@@ -1,10 +1,10 @@` means start with first string further ten strings changed.

# Matching commits

## Appenging string to file

Command `echo` output that there is given to it. 

By combining `echo` with symbols `>>`, that must be written on the screen 
will be written to the file. 

```bash
$ cat file.txt
First string 

$ echo "Second string of file" >> file.txt
$ cat file.txt
First string 
Second string of file
```

Operator `>>` could use with any command with ouptut on the screen something.

Sole operator `>` redirect to file too but rewrite file whole. 

```bash
$ cat file.txt
First string 
$ echo "New string" > file.txt
$ cat file.txt
New string 
```

## Comparing commits 

`git diff %hashA% %hashB%` - it output instruction list how to convert 
state A to state B. If change plase between, instruction would reverse.

# Igniring of files 

Often there are files than don't need keep history changes. 

* In case hiden files
* In Git don't accepted to commit compillation results, sourse only.
* IDE can create file with individual settings of project. IDE others people could misbehaviour.

To ignore that files, it necessary create file `.gitignore` and write ignore files here.

## How to fill `.gitignore`

`.gitignore` - common text file. It add into root of repository and commit too.

Into `.gitignore` add files list or templates.

> [!NOTE]
> Rules `gitignore` apply a new files (untracked) only.
If file get in staging area already, rules don't apply.

## Commentary 

If string starts with `#` - it is a commentery. `gitignore` don't get into account it.

## Plain file name

```
# for MacOS
.DS_Store
```
This way Git will ignore files with name `DS_Store` in the root and nested folders. 

## Asterisk (`*`)

Any string even empty.

## Question sign (`?`)

Any symbol.

## Square brackets 

Square brackets constist one symbol from list signed inside.

Enumeration symbols (`[abc]`) or dimesnion (`[a-z]`).

## Slash (`/`)

Slash indicates on catalogues. Is file starts with slash Git ignore all files or directories 
in root directory only.

`/todo.txt` - only root 

And `subdir/todo.txt` tracked. 

`spam.txt` - all folders.

If sample and with slash means rule apply to folder.

`build/` - ignore folder build.

## Couple astericks `**`

`**` - ignore several folder on way or zero.

`docs/**/tmp`

`*` - ignore one folder on the way

`docs/*/tmp`

## Invertion with exlamination sign (`!`)

## `.gitignore` and `git status`

Ignored files don't show in git status.

If we need output press `git status --ignored`. This way show up `Ignored files`.

# Clone repository

## Clone repository - `git clone`

We must got to GitHub repository, press **Code** and copy SSH key.

Further press in console `git clone %SSHLink%`.

To check if OK we can by `git remote -v`.

# Execute Fork 

If you want improve alien project. But you have not rights. You can copy repository 
to own repository on GitHub.

## What is Fork 

Results of operation Fork won't depict on source repository.

In process "fork" it is creating copy of all files and commiits and branches. 
This copy will store in your account.

Fork you cand do in GUI of GitHub.

# Branches 

# Why branch 

Branch is isolatet version of project.

Branches let to experiment with project in Git but preserve repository in stable state.
Every memver of the team can work in own branch and don't disturb others. 
Commits maden in one branch not visible in other. When work hte end branches possible 
to concatinate.

Branches useful for sole work. When write new features, need create new branch. 
That branches allow to swithch between task for one person.

## Show branches of project - `git branch`

# Creating branch - `git branch <new_brunch_name>

> [!NOTE] If slash exists in name of branch
> Name of branch can conclude letters and numbers, and four symbols `.`,`-`,`_`,`/`.
This symbols not mean something peculiar. Branches don't creating hierarchy. Like 
directory divided by slash `/`.

## Change branch - `git checkout <branch_name>`

## Create branch and right change to it `git checkout -b <branch name>`

# Comparing branches 

# Compare branches `git diff <branch_name1> <branch_name2>`

It possible use `git diff main <hash>`, also possible use indicator `HEAD`.

# Navigation suffix `~`

Navigation suffix `~N` count N commits back. Numeration starts with 0 (Zero).
`~0` - commit oneself.
 
`HEAD~1` further by temporary. `main~5` - fifth for branch `main`.

For `~1` there is chortcut `~`(without number).

# Branches merging 

## Fulfil merge - `git merge <branch_name>

First you must go to branch where we need add changes. Commonly it is main branch.

Goto main branch and execute `git merge` with merging branch like parameter.

## Delete branch after merging - `git branch -D <branch name>`

> [!NOTE]
> If you settle in branch wich want delete, it would error: `can not delete branch`.

`git branch -D` have safe mode with flag `-d`. It delete branch if it wholly merged with
another. Id est two branches become (or were) part of one history.

If you created a branch with incorrect name occasionally, you can delete it by
`git branch -d %branch_name%`.

> [!WARNING]
> Delting of local branch not delete repository branch.

# Collision

## How to solve a collision. Common recomendations.

During merging Git spotlight files, wich can't unit. To solve a problem it necessary:

1. Look file with conflict.
2. Learn both parts - your and your collegue. Your aim - to assemble two versions into final
and changes both parts don't loose. New version become actual.
3. Delete or amend inactual changes by hand, id it exist.
4. Prepare changes to saving and make a commit.

# Return to GitHub

## Send local branch to remote repository - `git push`

First commit another branch `git push -u origin <branch_name>`.

It is unnecessary to stay in consistence branch.

# Creating pull request

There is algorithm:

1. Work in own branch
2. End work and create pull request 
3. Your collegues check code and leave comments. This is **code review** or **review**
4. After final compliance you push your branch into the main.

## Parts of pull request and what could happen 

Every request have: 

* Name - short decription supposeded changes.
* Description - expanced description of changes. It is unnecessary.
* Source branch - where you work
* Aim branch - basic project branch where you want do changes.

Results of request:

* **merge** - supposeded changes accepted; code push into aim branch; pull request closing.
* **close** - pull request closing without merging changes.

