In Github we called changes as 'commit 

<h2>What is add in git?</h2>
add means that we made all needed change in the code.

<h2>what is commit in git?</h2>
commit means the addition of code is ready to change the code. And when we commit in repository it means the changes what we made is saved.Git save commits is the form of history.

How to make changes in git repository?

<h2>Configuring Git?</h2>

Configuration means we have to link Git software to our Github.<br />
We can configure a project as `Global` or `Local`. 

<h2>How to configure Code into git?</h2>

git config --global user.name "TaahaaUsman"
git config --global user.email "taha.usman.ccl@gmail.com"
git config --list : to show all congigured data

<h2>remote & local commands:</h2>
remote means GitHub website<br />
Local means the local machine of user.

<h2>Clone and Status</h2>

clone command is used to clone the folder into code editor 

```
git clone https://github.com/TaahaaUsman/Learn-Github.git
```

**Status** command is used to check the current status of folder. If we change the cloned folder wo 'git status' will show that the folder or files is modified. And we have to commit the changes.

```
git status
```

**There are four types of status:**<br />

untracked:
new files that git doesn't yet track 
<br>modified:
changed the existed file
<br>staged:
file is ready to be commit
<br>unmodified:
file is unchanged

<h2>Add & Commit comands</h2>

<h3>Add</h3>

using this command we adds the changed or new files in current working directory to the Git Staging area.
git add .\filename
git add . : is used to add multiple files in single click

<h3>Commit</h3>

It is record of changes and also saves the changes

```
git commit -m "Adding new file index.html"
```

<h3>Push command</h3>

This is used to upload the changes we made in our local machine. git push command make these changes to the github.

```
git push origin main
```


<h3>How to make changes in a folder which is Already placed at local machine</h3>

1. make a folder
2. run command `git init`
3. make changes
4. check the status of git using `git status`
5. run command `git add .`
6. run command `git commit -m 'Message`
7. go to the github make a new repository
8. run command `git remote add origin link_of_repo`
9. run command `git remote -v` <verify that the remote location is exit or not>
10. run command `git branch` <is used to show the names of brach>
11. run command `git branch -M main` <is used to rename the branch>
12. run command `git push origin main`

<h2>why  we use git push -u origin main</h2>

Because if we want to work in main branch for long time so, we use -u for telling the git that we will working in this branch for long.

### If any error occurs check the notes of shrada kapra ma'am

## Work Flow

Local Git

1. Cloning Git Repository
2. Make a GitHub Repository
3. clone it into folder
4. make changes
5. git add all 
6. git commit 
7. git push

## What are branches

We use branch concept in git to make it useable for multiple programmers. For example, we have a project and many people are working on the same project. So, every programmer make his own branch and make his neccassary changes and at the last point the all programmers merged there branch into main branch. This feather of github allow multiple user to work on a single project.

## Branch commands

1. git branch (is used to check the current working branch)
2. git branch -M main (is used to rename the current working branch)
3. git checkout branch_name (is used to switch from current working branch to othe branch)
4. git checkout -b branch_name (is used to make a new branch)
5. git branch -d branch_name (is used to delete an branch <we can'not delete branch where we are working>)

When we make our neccessary changes we have to push the branch to the gitHub. 

```
Command:
git push origin branch_name
```


# How to merge code from different branch

## Way 1
1. git diff branch_name (is used to compare branchs, commits, files or more)
2. git merge branch_name (is used to merge two branches)

## Way 2

1. Create a PR (Pull request)

## Pull command

pull command is used to fetch and download content from a remote repo into local machine. When we change a single branch and merge the branch to the main branch, then the changes were successfully made in the gitHub but it cannot come in the local machine, for downloading the changes to the local machine we use the pull command

```
git pull origin main
```

## Resolving Merge Coflicts

SomeTimes we made changes in two different branches and both changes make conflit because the change the same part of code. In this situation git will not be able to resovle this conflit. So, we have to resolve it by manually.
<br />
Simplly we have to use the tecnique of merging two different branches. When we try to merge two branches VS code will atomatically detect the conflit and give options to resolve it. Simplely follow the guide of VS code.

<Undoing Changes>
Sometimes we made some changes in the code which we don not have to. In this case we use some undoing commands to undo the doned operations.

case 1: staged changes (maybe we add some change which we do not want to so we use following commands)
    git reset file_name <will reset single file>
    git reset <will reset all files in the repository>
case 2: commited changes (for one commit)
    git reset HEAD~1
    HEAD~1 <means HEAD represent as the current pointer of changes, and it works like a queue. And we are saying in this command is that go back to 1 setp or HEAD>
case 3: commited changes (for many commits)
if we want to go mulple setps back so we use case 3 and following commads
    git reset Hash_value_of_commit <In this commad we copy the hash value of commit where we want to go and run the command>
    git reset --hard Hash_value_of_commit <using this commad these commits which are comes after the hash value will be removed form list>

git log <by using this command we check all changes and commits history>

<Fork command>
is used to copy other projects into a new repository. For example, some user make there React project code. So, we can use Fork for copying all that code into our own copyed repository.
Steps:
1- Search a repository into github
2- click on the option of Fork
3- Add name of Fork folder
4- After somethime the fork folder will be created