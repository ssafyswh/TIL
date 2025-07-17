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
- 마크다운: 일반 텍스트로 문서를 간단하게 작성하는 방법. 주로 개발자들이 텍스트와 코드를 작성해 문서화하기 위해 사용한다.
    - 문법
      - heading: "#"
      - list
      - code block
      - inline code block

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
