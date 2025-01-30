# 01- Setup & Configuration
- git config --global user.name "Your Name"
- git config --global user.email "your.email@example.com"
- git config --global core.editor "code --wait"  # Set VS Code as the default editor
- git config --list  # View all configurations

# 02- Initialize & Clone
- git init  # Initialize a new Git repository
- git clone <repo-url>  # Clone an existing repository
- git clone <repo-url> <folder-name>  # Clone into a specific folder

# 03- Branching & Switching
- git branch  # List all branches
- git branch <new-branch>  # Create a new branch
- git checkout <branch>  # Switch to an existing branch
- git checkout -b <new-branch>  # Create and switch to a new branch (old way)
- git switch <branch>  # Switch branch (new recommended way)
- git switch -c <new-branch>  # Create and switch to a new branch
- git branch -d <branch>  # Delete a local branch
- git branch -D <branch>  # Force delete a local branch

# 04- Staging & Committing
- git status  # Show status of changes
- git add <file>  # Stage a specific file
- git add .  # Stage all changes
- git commit -m "Your commit message"  # Commit changes with a message
- git commit --amend -m "Updated commit message"  # Edit the last commit message

# 05- Viewing History
- git log  # View commit history
- git log --oneline --graph --all --decorate  # View concise commit graph
- git log -p -2  # Show last 2 commits with changes

# 06- Undoing Changes
- git restore <file>  # Unstage changes (recommended over checkout)
- git checkout -- <file>  # Reset file to last committed state
- git reset HEAD <file>  # Unstage file but keep changes
- git reset --hard HEAD  # Reset all changes (WARNING: Cannot be undone)
- git revert <commit-hash>  # Create a new commit that undoes a previous one

# 07- Remote Repositories
- git remote -v  # View remote repositories
- git remote add origin <repo-url>  # Add a remote repo
- git push -u origin <branch>  # Push branch to remote
- git push origin --delete <branch>  # Delete a remote branch
- git fetch origin  # Fetch changes without merging
- git pull origin <branch>  # Pull latest changes from remote

# 08- Merging & Rebasing
- git merge <branch>  # Merge a branch into the current one
- git rebase <branch>  # Reapply commits on top of another branch
- git cherry-pick <commit-hash>  # Apply a specific commit from another branch

# 09- Tags
- git tag  # List all tags
- git tag <tag-name>  # Create a new tag
- git tag -a <tag-name> -m "Tag message"  # Create an annotated tag
- git push origin <tag-name>  # Push a tag to remote

# 10- Submodules
- git submodule add <repo-url>  # Add a submodule
- git submodule update --init --recursive  # Initialize and update submodules

# 11- Useful Shortcuts
- git diff  # View unstaged changes
- git stash  # Save changes temporarily
- git stash pop  # Reapply the last stash
- git shortlog -sn  # See contributors
- git clean -fd  # Remove untracked files & directories
