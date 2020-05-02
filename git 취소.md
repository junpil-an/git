soft - 현재 인덱스, 워킹트리를 유지한 채로 HEAD 변경

mixed - default 옵션, 인덱스는 취소한 채 워킹트리만 그대로

hard - 인덱스 워킹트리 변화 모두 제고 HEAD 변경



## git reset --soft HEAD^

- commit 한 부분을 취소하겠다

## git reset --hard @^

- hard를 이용해 HEAD 로 돌리는 명령어

## pull, merge 취소

git reset --hard ORIG_HEAD

git reset --merge ORIG HEAD

## git reset HEAD

default인 mixed를 이용해 HEAD로 돌아가게 하는 방법



작업할땐 항상 branch를 이용 추천,

