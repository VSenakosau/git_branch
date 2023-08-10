# Github_Homework 2
## 1. In your local repository, make branches for:
- Postman   
- Jmeter   
- Checklists   
- Bug Reports   
- SQL   
- Charles   
- Mobile Testing
-    
`To make branches on the local repository, you need to create a remote repository and clone it to the local computer`   
creating a remote repo called `git_branch`   
copying HTML link `https://github.com/VSenakosau/git_branch.git` to the remote repo     
cloning this repo to the local directory `git clone https://github.com/VSenakosau/git_branch.git`

To create branches, we use the `git branch` command. Let's execute the creation of all branches in one line using `&&`

`git branch Postman && git branch Jmeter && git branch Checklists && git branch Bug_Reports && git branch SQL && git branch Charles && git branch Mobile_Testing`   

Use the `git branch` command to verify that the branches have been created
```
vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (main)
$ git branch
  Bug_Reports
  Charles
  Checklists
  Jmeter
  Mobile_Testing
  Postman
  SQL
* main
```
## 2. Push all the branches to the remote repository.
vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (main)   
`git push origin --all`
```
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/VSenakosau/git_branch.git
 * [new branch]      Bug_Reports -> Bug_Reports
 * [new branch]      Charles -> Charles
 * [new branch]      Checklists -> Checklists
 * [new branch]      Jmeter -> Jmeter
 * [new branch]      Mobile_Testing -> Mobile_Testing
 * [new branch]      Postman -> Postman
 * [new branch]      SQL -> SQL
```
By using the `-u` flag (--set-upstream) when pushing your branches, Git remembers the remote tracking branches for you. This makes it easier to work with remote branches in the future because you don't need to remember or specify the remote and branch names each time you pull or push changes.   
vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (main)   
`git push -u origin --all`
```
Everything up-to-date
branch 'Bug_Reports' set up to track 'origin/Bug_Reports'.
branch 'Charles' set up to track 'origin/Charles'.
branch 'Checklists' set up to track 'origin/Checklists'.
branch 'Jmeter' set up to track 'origin/Jmeter'.
branch 'Mobile_Testing' set up to track 'origin/Mobile_Testing'.
branch 'Postman' set up to track 'origin/Postman'.
branch 'SQL' set up to track 'origin/SQL'.
branch 'main' set up to track 'origin/main'.
```
## 3. In Bug_Reports branch, create a text document with the structure of the bug report.
vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (main)   
`git checkout Bug_Reports`   
Switched to branch 'Bug_Reports'      
Your branch is up to date with 'origin/Bug_Reports'       

vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (Bug_Reports)      
`touch br_structure.txt`

vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (Bug_Reports)   
`nano br_structure.txt`      
Add information      
ctrl+O -> Enter (Save)         
ctrl+X -> Exit (Exit)      
## 4. Push the bug report structure to the remote repository
vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (Bug_Reports)   
`git add . `

vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (Bug_Reports)   
`git commit -m "Add br_structure.txt to Git"`   

vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (Bug_Reports)   
`git push`
```
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 793 bytes | 793.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/VSenakosau/git_branch.git
   0ad410c..c8d6408  Bug_Reports -> Bug_Reports
```
## 5. Merge Bug Reports branch into main
vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (Bug_Reports)   
`git checkout main`   
Switched to branch 'main'   
Your branch is up to date with 'origin/main'.   
 
vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (main)   
`git merge Bug_Reports`
```
Updating 0ad410c..c8d6408
Fast-forward
 br_structure.txt | 16 ++++++++++++++++
 1 file changed, 16 insertions(+)
 create mode 100644 br_structure.txt
```
## 6. Push main to the remote repository.
vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (main)   
`git status`
```
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```
vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (main)   
`git push origin main`
```
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/VSenakosau/git_branch.git
   0ad410c..c8d6408  main -> main
```
## 7. In the Checklists branch, create a file with checklist structure. 
vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (main)   
`git checkout Checklists`

vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (Checklists)      
`cat > Checklists_1.txt`   
```
1. Step number
2. Step title
3. Results
4. Comments
ctrl+D
```
## 8. Push a file with checklist structure to the remote repository
vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (Checklists)      
`git add .`

vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (Checklists)   
`git commit -m "Add file to Github"`

vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (Checklists)      
`git push`
```
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 342 bytes | 342.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/VSenakosau/git_branch.git
   0ad410c..f130744  Checklists -> Checklists
```
## 9. In the remote repository, do a pull request of Checklists branch into main
Go to GitHub website   
1. go to the `git_branch` remote repository   
2. in the branches, choose `Checklists`    
3. click on `Compare & pull request`    
4. add a comment (if you want)       
5. click on `Create pull request`   
6. on the next merge page, click on the `pull merge request` and `confirm the merge`
## 10. Synchronize remote and local main branches
vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (Checklists)   
`git checkout main`   
vvsen@Vadim MINGW64 /c/vadim/qa/github/git_branch (main)   
`git pull`
```
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (2/2), 746 bytes | 46.00 KiB/s, done.
From https://github.com/VSenakosau/git_branch
   c8d6408..71f0efe  main       -> origin/main
Updating c8d6408..71f0efe
Fast-forward
 Checklists_1.txt | 4 ++++
 1 file changed, 4 insertions(+)
 create mode 100644 Checklists_1.txt
```
