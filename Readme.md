# This file is for testing purpose of Git and GitHub

## Commands
# Basic Commands--<br>
  mkdir,
  rmdir,
  ls, 
  ls -a, (show all directories including Hidden)  
  pwd (show path)<br>

# Init Command--<br>
  git init, git add . , git status, git commit -m "commit name",<br>
  git remote add origin <-link->, git remote -v, git branch -M main(rename branch), <br>
  git push origin main/git push -u origin main(1st time), git push(after 1st time) <br>

# Clone Command--<br>
  git clone <-link-> 
  git clone <-link-> . (clone in current folder)

# Branch Command--<br>
  git branch(check branch), git branch -M main(rename), git checkout -b <-branchName->(create new branch),<br> 
  git checkout <-branchName->(navigate branches), git branch -d <-branchName->(delete branch)<br>
  git push origin <-branchName->

# Merging Branch--<br>
  Way1:<br>
      git diff <-branchName->
      git merge <-branchName->

  Way2:<br>
      create a PR(Pull Request)
      git pull origin main/git pull <-link->
