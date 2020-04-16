# GIT 

## git 명령어 

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

## git 설정

- `git init`으로 작업을 시작
```shell
git init
```
- `remote`: Git을 원격저장소에 저장하는 앤드포인트를 의미
```shell
git remote add origin https://github.com/username/name
```
- `git clone`로 주소 복사후 시작한다
```shell
git clone https://github.com/username/name
```
- 소스 업로드를 위해 `git add`를 사용
- ignore 파일이나 삭제한 파일 이력까지 commit 할 경우 `-f`옵션을 이용
```shell
git add *
git add * -f
```

- 소스를 commit하면 Staged상태의 파일이 history로 기록됨
 추적상태의 경우 `git status` 명령어를 이용해 확인
```shell
git status
```
- `git commit`명령을 통해 Staged 상태의 파일을 commit한다
  `-m`옵션으로 작성할 것을 권장
  `--amend` 다시 commit할 경우 덮어 씌울 수 있음
```shell
 git commit -m "저장할 내용"
```

## 소스 업데이트,commit된 내용 다운
 - 상대방이 commit한 파일은 명령어를 통해 직접 업데이트를 해야 동기화가 됨
 `git pull`,`git fetch`가 있음
 - `pull` 은 `fetch`+merge 작업이라 생각하면 됨
```shell
//matser branch를 pull하여 업데이트
git pull origin master

//master branch를 fecth하여 업데이트
git fetch origin master
```
## 소스 복원,리셋
- 실수로 잘못 작업하거나 예전 버전으로 롤백하여 적용할 경우 예전 버전으로 reset할 수 있음
```shell
git reset HEAD^ --soft
```
- `git reset` 다음 인수로는 되돌리는 버전의 위치
- 현재위치(HEAD)를 기준하여 상대적인 위치설정 or 특정 버전 리비전 고유 해시값을 지정
- HEAD 확인하고 싶으면 `git reflog` 이용
#### reset 용어
  -`--soft` : 약한특성 reset,되돌릴 때 기존의 인덱스와 워킹트리를 보존
  -`--hard` : 강한특성 reset,되돌릴 때 기존의 인덱스와 워킹트리를 버린다
  -`--mixed` :중간특성 reset,되돌릴 때 기존의 인덱스는 버리고 워킹트리는 보존
## Branch
  - git에서는 여러 갈래로 쪼개어 관리 가능
  - 기본은 master branch라고 불리며, 필수로 제공되는 branch
  - 서로 다른 브랜치들은 같은 조상을 가지고 있다
  - `git branch -n`으로 생성
  ```shell
  git branch new
  ```
  - master 기준으로 new를 branch하면 master와 똑같은 코드가  new에도 적용된다 
  - 하지만 new에서 코드를 수정하면 master와 new는 서로 다른 코드가 되어 갈라짐
  - 생성된 branch 로 접속하기 위해서는 `git checkout -n`를 이용
  ```shell
  git checkout new
  ```
  - 생성과 동시에 이동과정을 사용하고자 하면 `-b`를 추가
  ```shell
  git checkout -b new
  ```
  - 생성한 branch는 현재 로컬에 저장되어 있음
  - 생성한 branch를 원격저장소에 등록해주어야 함
  - `git push -n'를 이용 (-n : branch 이름)
  ```shell
  git push new
  ```
  - `git branch -d -n`로 branch 삭제
  ```shell
  git branch -d new
  ```
  -후에 삭제된 branch도 원격저장소에 반영을 해야함,branch 앞에 콜론(:)을 붙여주어야 함
  ```shell
  git push origin :new
  ```
##Git merge & rebase
  
  
  
