## git error 해결법


- ! [rejected]        master -> master (non-fast-forward)
  - 깃허브에 생성된 원격 저장소와 로컬에 생성된 저장소 간 공통분모가 없는 상태에서 병합하려는 시도로 인해 발생. 기본적으로 관련 없는 두 저장소를 병합하는 것은 안되도록 설정되어 있음
  - `git pull origin master --allow-unrelated-histories`를 추가해 두 저장소 병합하도록 사용
