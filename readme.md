# AI Master lecture materials

```bash
cd AI_Master_Lec

# Initialize git repository
git init

# Add remote repository
git remote add origin https://github.com/GithubJoshuaPark/AI_Master.git

# Add submodules for course materials
git submodule add https://github.com/GithubJoshuaPark/0_AI_Master.git 0_AI_Master
git submodule add https://github.com/GithubJoshuaPark/1_cv.git 1_cv
git submodule add https://github.com/GithubJoshuaPark/2_CNN.git 2_CNN
git submodule add https://github.com/GithubJoshuaPark/3_Object_detect.git 3_Object_detect

# Add files to the staging area
git add readme.md
git add .gitmodules

# Create the initial commit
git commit -m "Initial commit with submodules"

# Rename branch from master to main
git branch -M main

# Handle existing remote content (Method 1 - if you encounter conflicts)
# First attempt to pull with rebase
git pull --rebase origin main

# If you get conflicts:
# 1. Edit the conflicted files (like readme.md) to resolve conflicts
# 2. Mark as resolved
git add readme.md
# 3. Continue the rebase
git rebase --continue
# 4. Push to remote
git push --set-upstream origin main

# Alternative Method (Method 2 - if rebase is too complex):
# If you're still having issues, you can abort the rebase and use force push
# (Use with caution if others are working on the same repository)
git rebase --abort
# Then force push your changes
git push --force --set-upstream origin main

# Alternative Method (Method 3 - fresh start):
# If you want to start fresh but keep your work:
# 1. Backup your work
# 2. Fetch from remote
git fetch origin
# 3. Reset your local branch to match remote
git reset --hard origin/main
# 4. Apply your changes
# 5. Commit and push normally
```