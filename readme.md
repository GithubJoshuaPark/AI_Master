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
git submodule add https://github.com/GithubJoshuaPark/4_RL.git 4_RL
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

---

> I want to git clone git remote repository in my laptop pc.
> I wonder the remote repository has submoduels like the attached image.
> How can I pull the submodules as well?
>
> ✅ 방법 1: 한 번에 전체 클론 + 서브모듈 초기화
> ```bash
> git clone --recurse-submodules https://github.com/GithubJoshuaPark/AI_Master.git
>
>```
> <br>
> ✅ 방법 2: 기존 클론 후 서브모듈 수동 초기화
>
> ```bash
> git clone https://github.com/GithubJoshuaPark/AI_Master.git
> cd AI_Master
> git submodule init
> git submodule update
> ```

