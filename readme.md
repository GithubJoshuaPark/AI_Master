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
git add .

# Create the initial commit
git commit -m "Initial commit with submodules"

# Rename branch from master to main
git branch -M main

git push -u origin dev

# make dev branch from the current branch
git checkout -b dev

# push dev into remote repository
git push -u origin dev

# list the current branches
git branch | tail -f

```
>* dev
   main
```


```