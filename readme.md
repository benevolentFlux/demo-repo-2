## Prerequisites

credentials

    benevolentFlux@protonmail.com
    fluxation@github
    https://www.youtube.com/watch?v=RGOj5yH7evk 00:30:30

git 

    global information tracker
    version control system (CLS)
    version control interface (CLI)
    management of changes regarding ...
        - documents
        - programs
        - source code
        - algorithms
        - web sites
        - information
 
github

    website to host yout GIT repository online

## Commands

git version control:

    [pwd] > git --version
    [pwd] > git config -h
    [pwd] > git config --help
    [pwd] > git config --list --show-origin

configuration settings:

    [pwd] > git config --global user.name "username"
    [pwd] > git config --global user.email email.address@protonmail.com
    [pwd] > git config --global core.editor "code --wait"
    [pwd] > git config --global core.autocrlf input
    [pwd] > git config --global -e

create a project:

    [pwd] > mkdir foldername
    [pwd] > cd foldername
    [pwd] > git init
    [pwd] > open .git (not recommended)
    [pwd] > rm -rf .git (not recommended)

change repository

    [pwd] > git remote

push & pull files (repository):

    [pwd] > git commit -m "1st commit: initial code"
    [pwd] > git commit -m "2nd commit: refactored code"
    [pwd] > git commit -m "3rd commit: removed unused code"
    [pwd] > git commit -a -m "4rd commit: combined staging and committing"
    [pwd] > git push origin master
    [pwd] > git pull

push & pull file (staging area snapshot):

    [pwd] > git add refactored_file_01.txt refactored_file_02.txt
    [pwd] > git add deleted_file_00.txt
    [pwd] > git add *.txt
    [pwd] > git add .

repository status:

    [pwd] > git status

ssh-keyring:

    [~] > ssh-keygen -t rsa -b 4096 -C "email.address@github"
    [~] > ssh-agent sh -c 'ssh-add; ssh-add -L'
    [~] > cat ~/.ssh/id_rsa.pub
    [~] > ssh -T git@github (enter passphrase)
    [~] > eval "$(ssh-agent -s)"
    [~] > ssh.add ~/.ssh/ssh private key
    [~] > cd ~/etc/ssh/code ssh_config
    [~] > ssh-keyscan -t rsa github.com | ssh-keygen - lf -
    
    ~/.ssh/config
    [...]
    Host github.com
        User git
        Hostname github.com
        PrefferedAuthentications publickey
        IdentityFile ~/.ssh/id_rsa (<-)
        AddKeysToAgent yes (<-)
        UseKeychain yes (<-)

display the remote branches:

    [pwd] > git branch
    [pwd] > git checkout -b master

commit data stored:

    ID > - unique revision number
    message > - what was changed
    date & time > - when it was changed
    author > - by whom it was changed
    complete snapshot > - project full-content status
    compression > - git compresses the content of each commit
    duplicate > - git doesn't store duplicate content

status bar definitions:

    ![x] - changes not staged for commit
    ?[x] - untracked files
    +[x] - changes to be commited
     [x] - modified branch ready to git push (publication)

recommended use:

    [pwd] > cd <foldername>
    [pwd] > git init
    [pwd] > git status
    [pwd] > git add .
    [pwd] > git commit -m "commit title" -m "commit desription box message"
    [pwd] > git push origin master