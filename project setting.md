#프론트엔드 project 중 해야할 것들
## 1. 소스코드 초기 세팅
- create-react-app 기반 , sass, react-router-dom , eslint, prettier 등 설치
- 디렉토리 구조 세팅(ex.pages, components)
- 초기 설정(ex, routed.js 해놓기,service-worker, logo.svg 삭제 등등)

## 2.소스코드 초기세팅이 끝난 파일들 내 컴퓨터로 clone
- cmd에서 진행
- git clone https://github.com/username/name 

## 3.branch 만들기
- git branch -> branch 확인(내가 속한 branch 확인)
- git branch feature/login -> 새로운 branch 만들기(branch는 페이지별로 따야함??)
  똑같은 거로 만들면 충돌남
 -git checkout 이동할 branch 명 -> 새로 만든 branch로 이동
 -git branch -> 현재 어느 branch인지 재확인
 
## 4.코드들 수정 후 ,Git에 올려야 한다(push)
 - git add.(중간저장하는것)
 - git comment -m '메세지(수정한 내용 적기)
 - git push origin 브랜치명(feature/자기이름)
 
## 이 과정 후 팀 repository로 가서 pull request를 클릭해 수정내용을 적고 pr을 올림
 - pr 자세하게 어떤어떤 내용을 수정했는지 적음
 - base : 어디에 pull request 할 건지
 - compare : 자기 branch
 - pull request 누르면 초록색으로 뜸
 - 이후 merge 되면 끝~
 - 중간 중간 merge들로 변경된 코드들을 컴터에 다운받기 위해서는 
`git pull origin master`해주면 됨(중간중간 자주해주기)
 - push했을 때 routes에서 가장 충돌이 많이 남
 - 조금 더 공부가 필요하닷~!

 -
