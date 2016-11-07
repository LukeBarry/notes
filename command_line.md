commands covered in the command line lesson.

pwd = "print working directory."
ls ~ = list the files in our home directory
ls . = the directory we are currently in
ls .. = the directory above us
mkdir = make a directory
cp = copy
cd ~/ = move into the directory you want to move too.
mv = move a directory or rename a directory
rm = remove a directory
-r = this means to do the argument and all of the folders and files below it.
ctrl k clear cons

git init = initialize a repository
git status = checks to see what git sees....sort of like pwd for git
git add = adds untracked files to the repository so that they are now tracked
git commit = stores this particular snapshot of your project
git commit -m "description title" = the -m option is used to give a description of what changes you made to the commit.
git remote add origin https://github.com/LukeBarry/stats.git = add the github repository as a remote to your local git repository
git push -u origin master = pushes the changes to the remote repository #-u origin is github and master is a branch where we are putting commits
    the -u is saying always push origin and master together
git pull = pull from a remote repostiory

git checkout -b <branch_name> = This command tells Git to create a new branch (-b) called test_merge and switch to using that branch for commits
git commit -am  = -a tells Git to add all changes to previously committed files and saves us having to add them explicitly with git add
... like we did when we first committed the file. The -m tells Git to take the following text and insert it as a commit message.

git push --set-upstream origin <branch_name> = --set-upstream tells Git to set the remote server to test_merge based on origin

http://rogerdudler.github.io/git-guide/  # git simple guide

https://guides.github.com/introduction/flow/ # guide to github workflow
