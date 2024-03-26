# This file is for testing purpose of Git and GitHub
## Commands

# Basic Commands--<br>

  echo,
  mkdir,
  rmdir,
  ls,
  ls -a (show all directories including Hidden),
  touch <filename>,
  cat <filename>,
  pwd (show path),<br>
  git log (show all commits)/git log -5(show last 5 commits),<br>
  git log --oneline(show commits in one line)<br>
  git show <-commitHash-> (show change happend on that commit)

# Edit file in Bash Terminal--<br>
  vi/vim <filename> (open file in vim editor)<br>
  press i (for insert mode), esc (exit insert mode)<br>
  To save `:x` or `:wq` (which stands for "write" and "quit") and Enter <br>
  Leave without save `:q!` and Enter


# Init Command--<br>

  git init, git add . , git status, git commit -m "commit message",<br>
  git commit --allow-empty -m "commit message"(push empty commit),<br>
  git commit --amend / git commit --amend --no-update /git commit --amend -m "message"(to edit last commit without deleteing and it changes previous commit refs(shouldn't use in public repos))<br>
  git remote add origin <-link->, git remote -v, git branch -M main(rename branch), <br>
  git push origin main/git push -u origin main(setting upstream 1st time), git push(after 1st time) <br>
  git push origin main -f (forced push)<br>

# Clone Command--<br>

  git clone <-link->
  git clone <-link-> . (clone in current folder)

# Branch Command--<br>

  git branch(check branch), git branch -M main(rename), git checkout -b <-branchName->(create new branch),<br>
  git checkout <-branchName->(navigate branches), git branch -d <-branchName->(delete branch)<br>
  git push origin <-branchName->

  <mark>-For every new bugs, features, etc create a new branches because one branch can allow 
  one pull request at a time.</mark>


# Stash Command--(temporarily store changes in bg that are not ready to be committed)<br>
  git stash,<br>
  git stash pop,<br>
  git stash clear<br>

# Merging Branch--<br>

Way1:<br>

# Also used to solve merge conflicts.

      git diff <-branchName->,
      git merge <-branchName->

Way2:<br>
  create a PR(Pull Request),<br>
  git pull origin main/git pull <-link->

# Undoing Changes--<br>

To undo code changes:
  git restore --staged <-filename->, git restore<br>

Case1:staged changes <br>
  git reset <-fileName->,
  git reset
<br>
Case2:commited changes(for one)<br>
  git reset HEAD~1,<br>
  git reset --hard HEAD~1 (commit and code change both with reset),<br>
  git reset --soft HEAD~1 (only commit will reset but code change will still remains)<br>
Case3:commited changes(for many)<br>
  git reset <-commitHash->,<br>
  git reset --hard <-commitHash->, <br>
  git reset --soft <-commitHash-> (only commit will reset but code change will still remains)<br>

# Fork--<br>
  git remote add upstream <-url-> (adding upstream url)
  # Sync fork--<br>
     first select main branch ,then
     git fetch --all --prune and git reset --hard upstream/main
	OR
     git pull upstream main

# Interactive Rebase Commands--<br>
  
  git rebase -i <--commit hash-->(used to merge various commits, change messages, drop commits etc)<br>
  Ex: to whom, commits will merge choose it as `pick` those who will merge, change them to `s` or `squash`. Then write commit message<br> 

# Cherry Picking--<br>
    git cherry-pick <--commit hash-->

# Reflog--<br>
    git reflog
   Ex: git branch feature <--commit hash-->/ git reset <--commit hash-->
  <br>(used to see all history including reset, delete etc, using hash deleted commits, branches can retrieve)

# Search & Find--<br>
  by date:
  	--before / --after
  Ex: git log --after="2024-3-20"
  by message: 
  	--grep
  by author:
  	--author
  by file:
  	-- <filename>
  by branch:
  	<branch-A>

# Remove Commands--<br>

  git rm ( <filename> / * ) <br>
  git rm -rf <filename> (!forcefully and recursively remove the file without asking for confirmation so use carefully )<br> 
  git rm -r (Recursively removes folders) --cached (Removes the file only from the Git repository, but not from the filesystem) <br>
  git rm --dry-run (No files are actually removed) <br>
