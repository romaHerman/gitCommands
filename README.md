# gitCommands

1)
#init repo 
echo "# gitCommands" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/<YOU_REPO_NAME>/gitCommands.git
git push -u origin master

2)
#creare branch from master
1) git checkout -b second-step
2) lets add one more file (copy readme and rename to testFile)
3) add test file to the repository. we have 2 options 
   - git add testFile.md
   - git add -A ("-A" is shortcut for "add all new files" in most cases this shortcut is used)
4) lets check current status with comand git status -s (we see A(added) near testFile, M near readme stands for Modified)
5) let's commit our changes   git commit -m'test file added' 
6) run git status -s . It should not print anything to console because all changes were commited (saved)
7) we can see our commit history in this branch by running git log (shift+Q to exit, arrows up and down to scroll the log)
8) now lets make sure we're on our side branch, run command: git branch
9) push this branch to git repo : git push origin second-step . Now we can open git repo in browser and see that we have 2 branches (master and repo) with different content 

3)
#merge side branch to master 

1) first let's go to master branch and pull latest changes (maybe our teammates did some changes while we were working inside second-step branhc)
   - git checkout master 
   - git pull 
2) now we can got back to our branch 
   - git checkout second-step
3) and rebase (merge and put our changes on top ) our branch against master
4) now we can go to master and merge our branch to master
