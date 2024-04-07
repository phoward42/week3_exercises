Overview of the basic Git workflow:

# Load the current Git module
module load git/2.39.0

# Start a new Git repo
git init
(create a new directory as needed beforehand)

These directories are often hidden files, use this command to see them:
ls -a

# How to check status (and do so regularly)
git status

# Stage files for tracking
git add

Other options include:
*Stage all files in the project (either option works):*
git add --all
git add *

*Stage all files in a specific dir (here: 'scripts') in the project:*
git add scripts/*

*Stage all shell scripts *anywhere* in the project:*
git add *sh 

# Push files to local repo
git commit -m "commit message"
(must include -m with descriptive text when committing)

the "-a" command can be used to stage AND commit all changes at the same time, eg:
git commit -am "commit message"

# Check commit history 
git log
OR
git log --oneline

# Ignoring files and directories 
echo "data/" > .gitignore
echo "*~" >> .gitignore

git add .gitignore
git commit -m "Added a gitignore file"

# Moving and removing tracked files
git rm file-to-remove.txt
git mv myoldname.txt mynewname.txt
