I've updated the list to include the additional commands you provided while keeping the descriptions concise.  

---

### **Basic Git Commands with Descriptions**  

#### **Configuration**
- `git config --global user.name "Your Name"` → Set user name  
- `git config --global user.email "you@example.com"` → Set user email  
- `git config --list` → View Git configuration  

#### **Initializing and Cloning**
- `git init` → Initialize a new Git repository  
- `git clone <repo_url>` → Clone a repository  
- `git remote -v` → List remote repositories  
- `git remote add origin <repo_url>` → Add a remote repository  

#### **Branching and Switching**
- `git branch` → List local branches  
- `git branch -a` → List all (local & remote) branches  
- `git branch <branch_name>` → Create a new branch  
- `git checkout <branch_name>` → Switch to a branch  
- `git checkout -b <branch_name>` → Create and switch to a new branch  
- `git switch <branch_name>` → Switch to a branch (alternative to checkout)  
- `git switch -c <branch_name>` → Create and switch to a branch  
- `git push --all origin` → Push all branches to remote  

#### **Staging and Committing**
- `git status` → Check the status of the working directory  
- `git add <file>` → Stage a specific file  
- `git add .` → Stage all changes  
- `git commit -m "message"` → Commit staged changes  
- `git commit --amend -m "new message"` → Modify the last commit message  

#### **Merging and Rebasing**
- `git merge <branch_name>` → Merge a branch into the current branch  
- `git rebase <branch>` → Reapply commits on top of another branch  

#### **Pushing and Pulling**
- `git push origin <branch_name>` → Push changes to a remote branch  
- `git push -u origin <branch_name>` → Push and set upstream branch  
- `git push --all origin` → Push all branches  
- `git pull` → Fetch and merge remote changes  
- `git fetch origin` → Fetch latest changes without merging  

#### **File Management**
- `git rm <file>` → Remove a file from both working directory & repository  
- `git rm --cached <file>` → Remove file from tracking but keep in working dir  
- `git mv <old_name> <new_name>` → Rename a file and track the change  

#### **Viewing Changes and History**
- `git diff` → Show unstaged changes  
- `git diff --staged` → Show staged changes  
- `git log` → View commit history  
- `git log --oneline` → View commit history in one line  
- `git log --online` → Alternative shorthand for single-line log (typo in Git, should be `--oneline`)  
- `git show <commit_hash>` → View changes in a specific commit  

#### **Undoing Changes & Rollback**
##### **First-Level Rollback (Before Staging)**
- `git diff` → Show differences in modified files  
- `git checkout -- <file>` → Discard local changes to a file  

##### **Second-Level Rollback (After Staging)**
- `git diff --cached` → Show staged differences  
- `git restore --staged <file>` → Unstage a file  

##### **Rollback After Committing**
- `git revert HEAD` → Create a new commit that undoes the last commit  
- `git revert <commitID>` → Undo changes from a specific commit  
- `git reset --hard <commitID>` → Reset to a previous commit & remove commit history  

#### **Stashing**
- `git stash` → Save uncommitted changes  
- `git stash pop` → Apply stashed changes  
- `git stash list` → View all stashes  
- `git stash drop` → Delete a stash  

#### **Cleaning**
- `git clean -n` → Show files that would be deleted  
- `git clean -f` → Delete untracked files  

#### **Tagging**
- `git tag <tag_name>` → Create a new tag  
- `git tag` → List all tags  
- `git tag -d <tag_name>` → Delete a tag  
- `git push origin <tag_name>` → Push a tag to remote  

---

This covers almost all essential Git commands, including the rollback options you mentioned. Let me know if you need any refinements! 🚀
