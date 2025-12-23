# How to Use Git and Github

## Stages

  a. Working Directory → where init the git, changes tracked to loc repo
  
  b. Staging Area (untracked/tracking/
  
  c. Local Git Repo
  
  d. Remote Git Repo 
  

Local Repo

 Preparation by creating a file or select folder

1. initialize git with, see with ls-a details, this .git file will have all content on tracking in
         shown with $git status
    → shows now untracked files which are not tracked
 $git init 
2. tracking files into staging area with, dot  .  adds all files in folder
  ($git add file.xyz)
  $git add .
3. commit under version control, message in present tense
 $git commit -m “init”
  can see what commits $git log
    
    to roll back to last version tracked in git repo into working dir 
              $git checkout chapter3.txt
    
    differences to files
               $git diff chapter3.txt
    
    remove files, -r for recursive and . for all files
             $git rm —cached -r .
    

## Remote Repo

Github create repo with CLI

1. to let local git repo know a remote repo 
  $git remote add origin https://github.com/designovaone/Git_HowTo.git
2. push local repo to remote
$git push -u origin main

this is all main branch, network/commit show details and timing

 Git Ignore

To disable certain files, e.g. key file, sensitive files, API keys to be committed

DS_files are setting files shown

 A. create a file with
    $touch .gitignore

 B. add files to the .gitignore
    by adding to the file as is, or wildcard
     * . txt
     # is comment

C. Include
  to git by add and commit 

D. Templates from githut on github/gitingore 
      [https://github.com/github/gitignore](https://github.com/github/gitignore)  
      and search for type, e.g. node
      a. copy and add into .gitignore

Git Clone

copy to local by cloning to continue on ([examples OS](https://github.com/awesome-selfhosted/awesome-selfhosted?tab=readme-ov-file))

command is $git clone url

then follow instruction and can run often local, quake/wordle

Branching & Merging

A. create a new branch by name
  $git branch “name”
to see the branches $git branch and * shows active branch

B. to switch a branch
  $git checkout “name”

C.  Merge
  Modified both branches on added committed on main the current sets, to merge
  got to main branch and merge the side-path to it
  $git merge name-of-branch

  this opens VIM for notes, to close :q to quit
  check by git log
  → now shows Merge branch ‘side-path’

D. Push
  to remote 
  $git push origin main -u
  
Additionally on GitHub there are graphical representation on github Insights/Network

More Learning 

[https://learngitbranching.js.org](https://learngitbranching.js.org/)
