- GUI(Graphing User Interface)
: **그래픽**을 통해 사용자와 컴퓨터가 상호 작용하는 방식

- CLI(Command Line Interface)
: **명령어**를 통해 사용자와 컴퓨터가 상호 작용하는 방식

- CLI 기초 문법
    - .: 현재 디렉토리
    - ..: 상위 디렉토리(부모 폴더)
    - touch: 파일 생성
    - mkdir: 디렉토리 생성
    - ls: 현재 작업중인 디렉토리 내 모든 디렉토리/파일 목록 호출(list)
    - cd: 현재 작업중인 디렉토리를 변경
    - start: 디렉토리 내 파일을 실행 혹은 디렉토리 열기
    - rm: 파일 삭제
    - rm -r: 디렉토리 삭제
    - pwd: 현재 작업중인 디렉토리의 절대 경로를 출력

- git: **분산** 버전 관리 시스템

- git의 영역
    - working directory
    - staging area
    - repository

- git command

    1. git init: .git 폴더 생성

    2. git add: 변경내역이 있는 파일을 staging area로 보내기

    3. git commit: staging area에 있는 변경 내역에 그 내용을 메모하기

    4. git push: commit이 완료된 내용을 repository로

    5. git clone: repository에 있는 파일을 그대로 로컬 저장소로 복제(.git 폴더 포함, **git init할 필요 없음!**)
    
    6. git pull: repository와 변경내역만을 받아오기

- gitignore: 디렉토리 내에 있는 파일 중 repository로 보내고 싶지 않은 파일의 목록을 작성

- revert & reset
    - git revert: 특정 commit을 없었던 일로 만드는 작업 <br> ```git revert <commit id>```
    - 단일 commit을 실행 취소, 그 후 그 결과를 새로운 commit으로 추가
    - commit 자체를 삭제하는 것이 아니라, 그 commit을 취소하는 새로운 commit을 추가함으로써 기록의 손실을 방지하며 기록의 무결성과 협업의 신뢰성을 높인다.
    - 추가 명령어(참고만 할것)
    - 공백을 사용하여 여러개의 commit을 한번에 실행 취소 <br> ```git revert <commit id_1> <commit id_2> ...```
    - '..'을 사용해 범위를 지정하여 다수의 commit을 한번에 실행 취소(가급적 사용할 일이 없게 할것) <br> ```git revert <commit id_1>..<commit id_n>```
    - commit 메시지 작성을 위한 편집기를 열지 않기 (자동 commit 진행) <br> ```git revert --no-edit <commit id>```
    - 

※ git rm --cached와 git restore --staged의 차이? (교안과 다소 차이 있음)
