# Markdown
- 마크다운: 일반 텍스트로 문서를 간단하게 작성하는 방법. 주로 개발자들이 텍스트와 코드를 작성해 문서화하기 위해 사용한다.
---
- 문법
    - heading: 문서의 단계별 제목으로 사용. #\의 개수에 따라 제목의 수준을 구별한다.<br> #의 개수가 많을 수록 소제목이다.
    - list: 목록을 표시하는 기능. 순서가 있는 목록은 내용 앞에 1. , 2. , ... 으로 표기하며 순서가 없는 목록은 - 으로 표기한다.<br> 탭을 사용하여 하위 목록을 제작하는 것도 가능하다.
    - code block: 해당 프로그래밍 언어에 맞춰 텍스트 스타일을 변환한다. SW 개발에서 마크다운을 사용하는 가장 큰 이유 중 하나. 코드의 끝과 시작에 백틱(`)을 3개씩 표기하여 사용한다.<br> ```print("Hello world!")```
    - link & image: 특정 주소를 사용해 다른 페이지로 이동하는 링크 혹은 이미지를 출력<br>
```[사이트 이름](링크)``` <br>
```![이미지 이름](경로)``` <br>
이 때, 이미지의 너비와 높이는 마크다운으로는 조절할 수 없다. (HTML 필요)
    - 텍스트 관련 문법: <br>
      **굵게** ```**굵게**``` <br>
      *기울임* ```*기울임*``` <br>
      ~~취소선~~ ```~~취소선~~```
    - 수평선: 단락을 구분하기 위해 사용 ```---```
---
- 그 외의 문법은 [마크다운 가이드](https://www.markdownguide.org/basic-syntax) 활용하기
git push test