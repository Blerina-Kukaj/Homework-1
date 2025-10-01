# Homework #1: Git Workflow and History Management  

1. Initialized a new repository with `git init`.  
2. Added `project.txt` and made several commits with unclear messages (`update`, `stuff`, `final`).  
3. Cleaned up the history with `git rebase -i`:  
   - Renamed the first commit from `update` → **Initial commit**.  
   - Squashed the third commit (`final`) into the second commit (`stuff`).  
   - Renamed the new combined commit to **Add practice lines and finalize homework**.  
4. Simulated a mistake by committing an extra change, then removed it with `git reset --hard`.  
5. Recovered the lost commit using `git reflog` and `git checkout <commit-hash>`.  
6. Created a new branch `new-branch` from the recovered commit with `git switch -c new-branch`.  
7. Configured a custom alias `git lg` to view commit history in a visual graph format:  

   ```bash
   git config --global alias.lg "log --color --graph --pretty=format:'%C(yellow)%h%C(reset) - %C(cyan)%an%C(reset) %C(green)(%ar)%C(reset) %C(white)%s%C(reset) %C(red)%d%C(reset)' --all"
'
   8. Tagged the cleaned-up commit on `new-branch` as `v1.0`:
