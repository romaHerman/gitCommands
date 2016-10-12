
# gitCommands

#0 
open github your github accaunt and create new, empty git repo 

1)
#init repo 
create folder on your desctop (e.g. gitTest), 
then open terminal, navigate to this folder (e.g. cd ~/Desktop/gitTest)
print this in terminal

1) echo "# gitCommands" >> README.md
2) git init
3) git add README.md
4) git commit -m "first commit"
5) git remote add origin https://github.com/<YOU_REPO_NAME>/gitCommands.git
6) git push -u origin master

2)
#creare branch from master
1) git checkout -b second-step \n
2) lets add one more file (copy readme and rename to testFile) \n
3) add test file to the repository. we have 2 options \n
   - git add testFile.md
   - git add -A ("-A" is shortcut for "add all new files" in most cases this shortcut is used) \n
4) lets check current status with comand git status -s (we see A(added) near testFile, M near readme stands for Modified) \n
5) let's commit our changes   git commit -m'test file added' \n
6) run git status -s . It should not print anything to console because all changes were commited (saved) \n
7) we can see our commit history in this branch by running git log (shift+q to exit, arrows up and down to scroll the log) \n
8) now lets make sure we're on our side branch, run command: git branch \n
9) push this branch to git repo : git push origin second-step . Now we can open git repo in browser and see that we have 2 branches (master and repo) with different content  \n

3)
#merge side branch to master 

1) first let's go to master branch and pull latest changes (maybe our teammates did some changes while we were working inside second-step branhc)
   - git checkout master 
   - git pull \n
2) now we can got back to our branch \n
   - git checkout second-step
3) and rebase (merge and put our changes on top ) our branch against master \n
4) now we can go to master and merge our branch to master git merge --no-ff second-step \n
   vim will be opened after merge. to exit press shift+q, then type wq! and press enter. \n
5) and then we can push our changes to master git push origin master \n
