HTML

CSS
javascript
2.1 backand technologies
1.java
2.python
3.node
“this is paragraph”
this paragraph
content in italic and bold
function add(x,y) {
return x+y
}
}
‘’’’
“git branch”
flower pic?
{facebook}https://en-gb.facebook.com/
quote

table
s.no	name	age
1.	likitha	19
2.	nageswaramma	69
3.	lakshmana rao	72
Capital of AP

DESCRIPTION
This tutorial explains how to import a new project into Git, make changes to it, and share changes with other developers.

If you are instead primarily interested in using Git to fetch a project, for example, to test the latest version, you may prefer to start with the first two chapters of The Git User’s Manual.

First, note that you can get documentation for a command such as git log --graph with:

$ man git-log
or:

$ git help log
With the latter, you can use the manual viewer of your choice; see git-help[1] for more information.

It is a good idea to introduce yourself to Git with your name and public email address before doing any operation. The easiest way to do so is:

$ git config --global user.name "Your Name Comes Here"
$ git config --global user.email you@yourdomain.example.com
Importing a new project
Assume you have a tarball project.tar.gz with your initial work. You can place it under Git revision control as follows.

$ tar xzf project.tar.gz
$ cd project
$ git init
Git will reply

Initialized empty Git repository in .git/
You’ve now initialized the working directory—​you may notice a new directory created, named ".git".

Next, tell Git to take a snapshot of the contents of all files under the current directory (note the .), with git add:

$ git add .
This snapshot is now stored in a temporary staging area which Git calls the "index". You can permanently store the contents of the index in the repository with git commit:

$ git commit
This will prompt you for a commit message. You’ve now stored the first version of your project in Git.

Making changes
Modify some files, then add their updated contents to the index:

$ git add file1 file2 file3
You are now ready to commit. You can see what is about to be committed using git diff with the --cached option:

$ git diff --cached
(Without --cached, git diff will show you any changes that you’ve made but not yet added to the index.) You can also get a brief summary of the situation with git status:

