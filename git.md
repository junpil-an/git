# GIT 

## 1.git 정리

- git init : git 생성하기
- git clone git_path : 브랜치 선택하기(주소입력)
- git checkout -t remote_path/branch_name : 원격 브랜치 선택하기
- git branch -r : 원격 브랜치 목록보기
- git branch -a : 로컬 브랜치 목록보기
- git branch -m branch_name change_branch_name : 브랜치 이름 바꾸기
- git branch -d branch_name : 브랜치 삭제하기
- git push remote_name --delete branch_name : 원격 브랜치 삭제하기
- git add file_path :수정한 코드 선택하기(git add *)
- git commit -m "수정 내용" :코드 설명 적기
- git push remote_name branch_name: add 하고 commit한 코드 git server에 보내기
  (git push origin master)
- git pull - git서버에서 최신코드 받아오기 & merge
- git fecth - git 서버에서 최신코드 받아오기
- git reset --hard HEAD^ :commit 한 이전 코드 취소
- git reset --soft HEAD^ :코드는 살리고 commit만 취소하기
- git reset --merge : merge 취소하기
- git reste --hard HEAD && git pull: git 코드 강제로 받아오기
- git config --global user.name "user_name" :git계정 NAME 변경하기
- git config --global user.emai "user_email" :git계정 Email 변경하기
- git stash/git stash save "description" : 작업코드 임시저장, branch 바꾸기
- git stash pop :마지막으로 임시저장한 작업코드 가져오기

 '''shell
 
 git config --
'''



 ```shell
    git clone https://github.com/KennethanCeyer/tutorial.git
```



