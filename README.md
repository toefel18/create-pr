# create-pr

Simple bash script that creates a PR from your current staging area!


Example: 2 files changed, but only README.md is added to staging area
```bash
$ git st
  On branch master
  Your branch is up to date with 'origin/master'.
  
  Changes to be committed:
    (use "git reset HEAD <file>..." to unstage)
  
  	modified:   README.MD
  
  Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git checkout -- <file>..." to discard changes in working directory)
  
  	modified:   build.gradle
```

At this point, you can simply run `create-pr` to create a PR for README.md, it will use commit message `quick pr`.

You can optionally provide a commit message, for example `create-pr LOY-S964 updated versions`

```bash
$ create-pr LOY-S126 updated versions
  you are currently on master
  using message LOY-S126 updated versions
  on master, creating a new branch create-pr-6083-15408
  M	README.MD
  M	build.gradle
  Switched to a new branch 'create-pr-6083-15408'
  Committing staged files with message LOY-S126 updated versions
  [create-pr-6083-15408 b597820] LOY-S126 updated versions
   1 file changed, 2 insertions(+)
  Warning: 1 uncommitted change
  Counting objects: 3, done.
  Delta compression using up to 8 threads.
  Compressing objects: 100% (3/3), done.
  Writing objects: 100% (3/3), 309 bytes | 309.00 KiB/s, done.
  Total 3 (delta 2), reused 0 (delta 0)
  remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
  remote: 
  remote: Create a pull request for 'create-pr-6083-15408' on GitHub by visiting:
  remote:      https://github.com/intergamma/loyaltypointmicroservice/pull/new/create-pr-6083-15408
  remote: 
  To github.com:intergamma/loyaltypointmicroservice.git
   * [new branch]      HEAD -> create-pr-6083-15408
  
  Creating pull request for create-pr-6083-15408 into master in intergamma/loyaltypointmicroservice
  
  created PR 80, opening browser
  Opening https://github.com/intergamma/loyaltypointmicroservice/pull/80 in your browser.
```

The PR will be created and your browser will be opened automatically!

# Installation

1. Install github cli: https://cli.github.com/manual/installation

1. Clone this REPO somewhere
       
       cd $HOME
       git clone https://github.com/toefel18/create-pr.git 
       
1. Add the bin folder to your PATH (save this in .bashrc)

       PATH=$PATH:$HOME/create-pr/bin
       
