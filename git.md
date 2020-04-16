# GIT 

## 1.git 정리

- `git init` : git 생성하기
- `git clone git_path` : 브랜치 선택하기(주소입력)
- `git checkout -t remote_path/branch_name` : 원격 브랜치 선택하기
- `git branch -r` : 원격 브랜치 목록보기
- `git branch -a` : 로컬 브랜치 목록보기
- `git branch -m branch_name change_branch_name` : 브랜치 이름 바꾸기
- `git branch -d branch_name` : 브랜치 삭제하기
- `git push remote_name --delete branch_name` : 원격 브랜치 삭제하기
- `git add file_path` :수정한 코드 선택하기(git add *)
- `git commit -m "수정 내용"` :코드 설명 적기
- `git push remote_name branch_name`: add 하고 commit한 코드 git server에 보내기
  (git push origin master)
- `git pull` : git서버에서 최신코드 받아오기 & merge
- `git fecth` : git 서버에서 최신코드 받아오기
- `git reset --hard HEAD^` :commit 한 이전 코드 취소
- `git reset --soft HEAD^` :코드는 살리고 commit만 취소하기
- `git reset --merge` : merge 취소하기
- `git reste --hard HEAD && git pull`: git 코드 강제로 받아오기
- `git config --global user.name "user_name"` :git계정 NAME 변경하기
- `git config --global user.emai "user_email"` :git계정 Email 변경하기
- `git stash/git stash save "description"` : 작업코드 임시저장, branch 바꾸기
- `git stash pop` :마지막으로 임시저장한 작업코드 가져오기
- `git status` :변경된 것들이 있나 확인


## 2. 깃을 사용하는 이유
 - 빠른 협업환경
 - 누가 언제 수정했는지 코드리뷰 가능
 - IssueTracker 및 Migrate 연동 지원
 - GitHub 이용해 자신의 git을 쉽게 전파가능
 - Countinuous Integration(지속적인 통합) 지원
 - VS,Eclipse,Android S 등 많은 부분에서 Git 연동 제공
 - **협업을 위해 사용**

## 3. Git 사전지식
- commit :파일을 추가하거나 변경 내용을 저장소에 저장하는 작업
- push : 파일을 추가하거나 변경 내용을 원격저장소에 업로드 하는 작업
- branch : 독립적으로 어떤 작업을 진행하기 위한 개념, 각각의 branch는 다른 branch에 영향 x,여러 작업 동시 진행 가능
![명령어에 따른 전이표](https://jistol.github.io/assets/img/git/git-basic/git-basic-3.png)

