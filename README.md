# gitCommands

1)
#init repo 
echo "# gitCommands" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/romaHerman/gitCommands.git
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
7) we can see our commit history in this branch by running git log

