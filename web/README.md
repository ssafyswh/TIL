WWW(World Wide Web): 인터넷으로 연결된 컴퓨더들이 정보를 공유하는 거대한 정보 공간
웹: Web site, Web application 등을 통해 사용자들이 정보를 검색하고 상호 작용하는 기술
웹사이트: 인터넷에서 여러개의 웹페이지가 모인 것으로, 사용자들에게 정보나 서비스를 제공하는 공간
웹페이지: HTML, CSS 등의 웹 기술을 이용하여 만들어진, 웹사이트를 구성하는 하나의 요소
HTML(HyperText Markup Language): 웹페이지의 의미와 구조를 정의하는 언어
hypertext: 웹 페이지를 다른 페이지로 연결하는 링크
markup language: 태그 등을 이용하여 문서나 데이터의 구조를 명시하는 언어(예: HTML, Markdown)
- markup language의 적용 과정
  1. 구조와 형식 없이 내용이 나열되어 있는 데이터
  2. 사람이 이해할 수 있도록 논리적 구조를 부여
  3. 컴퓨터가 이해하고 화면에 표현항 수 있도록 약속된 언어로 구조를 만들기
  4. 웹 브라우저가 코드를 해석하여 사용자에게 웹 페이지를 출력함
HTML의 구조
- 예시
```html
<!DOCTYPE html>
<html land="en">
<head>
  <meta charset="UTF-8">
  <title>My page</title>
</head>
<body>
  <p>This is my page</p>
</body>
</html>
```
- ```<!DOCTYPE html>```: 해당 문서가 html로 문서라는 것을 나타냄
- ```<html></html>```: 전체 페이지의 콘텐츠를 포함하는 가장 상위의 태그
- ```<title></title>```: 브라우저 탭 및 즐겨찾기 시 표시되는 제목으로 사용
- ```<head></head>```: html 문서에 관련된 설명, 설정 등 컴퓨터가 식별하는 메타데이터를 작성. 사용자에게 보이는 영역은 아니다.
- ```<body></body>```: html 문서의 내용을 나타냄. 페이지에 표시되는 모든 콘텐츠를 작성하며 한 문서에 하나의 body 요소만 존재해야 한다.
- html element(요소)
  - 하나의 요소는 여는 태그와 닫는 태그, 그리고 그 안의 내용으로 구성된다.
  - 닫는 태그는 태그 이름 앞에 슬래시가 포함된다. (단, 닫는 태그가 없는 태그도 존재한다.)
- html attributes (속성): 사용자가 원하는 기준에 맞도록 요소를 설정하거나 다양한 방식으로 요소의 동작을 조절하기 위한 값.
  - 목적
    - 나타내고 싶지 않지만 추가적인 기능 혹은 내용을 담고 싶을 때 사용한다.
    - CSS에서 스타일 적용을 위해 해당 요소를 선택하기 위한 값으로 활용된다.
  - 작성 규칙
    - 속성은 요소 이름과 속성 사이에 공백이 있어야 한다.
    - 하나 이상의 속성들이 있는 경우엔 속성 사이에 공백으로 구분한다.
    - 속성 값은 열고 닫는 따옴표로 감싸야 한다.
    - 예시
    ```html
     <p class="editor-node">My cat is very grumpy</p>
    ```
  - ```<p></p>```: 텍스트 문단(paragraph)을 만드는 태그
  - ```<a></a>```: 다른 페이지로 이동시키는 하이퍼링크 태그. (anchor)
  - ```<img></img>```: src에 지정된 그림을 보여주는 태
- html text structure
  - html의 주요 목적 중 하나는 텍스트 구조와 의미를 제공하는 것이다.
  ```html
  <body>
    <h1>main heading</h1>
    <h2>sub heading</h2>
    <p>this is my page</p>
    <p>this is <em>emphasis</em></p>
    <p>Hi <strong>my name</strong> is air</p>
    <ol>
      <li>python</li>
      <li>algorithm</li>
      <li>web</li>
    </ol>
  </body>
  ``` 
  - heading & paragraphs: h1~6, p
  - lists: ol, ul, li
  - emphasis & importance: em, strong
웹 스타일링
- CSS(Cascading Style Sheet): 웹페이지의 디자인과 레이아웃을 구성하는 언어.
  - 적용 방법
    - 인라인(inline) 스타일
      - html 요소 안에 style 속성 값으로 작성하는 방법
      - style 속성 내부는 css 문법으로 작성한다.
      - 동일한 스타일을 사용하더라도 매번 다시 적어야 하기 때문에 불편하다.
    - 내부(inernal) 스타일 시트
      - head 태그 안에 style 태그를 작성하는 방법
    - 외부(external) 스타일 시트
      - 별도의 css 파일을 생성하고 html link 태그를 사용해 불러오는 방법
  - css 구문
    - 기본 구조와 문법
      - 선택자(selector): 무엇을 꾸밀지 지정하는 부분
        - 기본 선택자
          - 전체 선택자(*): html 모든 요소를 선택
          - 요소 선택자(태그 선택자): 지정한 모든 태그를 선택
          - 클래스 선택자(.): 주어진 클래스 속성을 가진 모든 요소를 선택
          - 아이디 선택자(#): 주어진 아이디 속성을 가진 요소를 선택. 단, 그 아이디를 가진 요소가 문서 내에 하나만 존재해야 한다.
          - 속성 선택자([]): 주어진 속성이나 속성값을 가진 모든 요소를 선택. 속성의 존재 여부, 깂의 일치/포함 등 다양한 조건으로 요소를 정교하게 선택할 수 있다.
        - 결합자(combinator)
          - 자손 결합자(" "(공백))
            - 첫번째 요소의 자손 요소들 선택
          - 자식 결합자(">)
            - 첫번째 요소의 직계 자식만 선택
      - 선언(declaration): 어떻게 꾸밀지에 대한 구체적인 한 줄의 명령. 속성과 값이 한쌍으로 이루어지며 세미콜론으로 끝내야 한다.
        - 명시도(specificity): 결과적으로 요소에 적용할 css 선언을 결정하기 위한 알고리즘
          - cascade: 계단식. 한 요소에 동일한 가중치를 가진 선택자가 적용될 때, css에서 가장 마지막에 나오는 선언이 사용된다.
          - 명시도 순서 기준
            1. importance: ```!important```
               - ※cascade의 구조를 무시하고 갈제로 스타일을 적용하는 방식이므로 가급적 사용을 권장하지 않는다. 
            2. inline 스타일
            3. 선택자(id 선택자 > class 선택자 > 요소 선택자)
            4. 소스 코드 선언 순서
      - 속성(property): 바꾸고 싶은 스타일의 종류를 나타낸다.
        - css가 미리 정의해 둔 키워드를 사용해야 한다.
        - ※ 종류가 정말 많기 때문에, 자동완성 기능 및 기능 검색을 적극적으로 활용할 것
          - 상속: 기본적으로 css는 상속을 통해 부모 요소의 속성을 자식에게 상속해 재사용성을 높인다.
            - 상속 가능한 속성: text 관련 요소, opacity, visibility
            - 상속 불가능한 속성: box model 관련 요소, position 관련 요소  
      - 값(Value): 속성에 적용할 구체적인 설정을 나타낸다.
        - 속성이 받을 수 있는 값의 종류가 속성마다 정해져 있다.
        - 값의 단위: 키워드로 끝나는 값도 있지만, 크기나 간격 등을 나타낼 때는 단위가 필수적이다.
          - 절대 단위: 다른 요소의 영향을 받지 않는 고정된 크기
            - "px": 화면을 구성하는 가장 작은 단위인 픽셀을 기준으로 하는 절대 단위. 모니터 해상도에 따라 크기가 결정되며, 직관적이고 예측이 쉽다.
              - 장점
                - 디자인 시안과 거의 동일한 결과물을 만들 수 있다.
                - 요소의 크기를 명확하게 고정하고 싶을 때 유용하다.
              - 단점
                - 사용자가 브라우저의 기본 폰트 크기를 변경해도 요소의 크기가 함께 조절되지 않아 접근성에 불리하다.
                - 다양한 디바이스 크기에 유연하게 대응하는 반응형 디자인에 한계가 있다.
          - 상대 단위: 다른 요소(부모, 화면 표시 영역 등)의 크기에 따라 상대적으로 결정되는 크기
            - "em": 부모 요소의 font-size를 기준으로 크기가 결정되는 상대 단위. 부모 요소에 font-size가 없을 경우, 상위 부모의 font-size를 상속 받는다.
              - 장점
                - 부모 요소의 크기에 따라 자식 요소의 크기를 유연하게 조절 가능하다.
              - 단점
                - 중첩 문제: em 단위를 사용하는 요소가 중첩되면 기준 크기가 계속 변경되어 계산이 복잡해지고 예측이 어려워진다. -> rem으로 해결 가능하다.
            - "rem" (root em): 부모 요소가 아닌, 최상위 요소인 ```<html>```의 font-size를 기준으로 크기를 결정한다.
              - html의 기본 font-size는 대부분의 브라우저에서 16px이다.
              - 장점
                - 일관성 및 예측 가능성: 요소가 아무리 깊게 중첩되어도 기준은 항상 html이므로 계산이 복잡해지지 않는다.
                - 유지보수 용이성: html의 font-size만 변경하면 사이트 전체의 레이아웃과 폰트 크기를 일관되게 조절할 수 있다.
                - 접근성 향상: 사용자가 브라우저에서 설정한 기본 폰트 크기를 html이 상속받으므로, 사용자의 설정에 맞춰 사이트 전체가 유연하게 확대/축소된다.
  - CSS Box Model: 웹페이지의 모든 html 요소를 감싸는 사각형 상자 모델
    - 박스 구성 요소
      - content: 실제 내용이 위치하는 영역
      - padding: content와 border 사이의 내부 영역
      - border: content와 padding을 감싸는 테두리
      - margin: 이 박스와 다른 요소와의 외부 간격
      - 구성 요소 별 속성
        - content: width, height
        - padding, border, margin: top, bottom, left, right
    - CSS Layout
      - 각 요소의 위치와 크기를 조정하여 웹페이지의 디자인을 결정하는 것. 요소들을 상하좌우로 정렬하고, 간격을 맞추고 전체적인 페이지의 뼈대를 구성한다.
      - display 속성
        - 박스 타입: 박스 타입에 따라 페이지에서의 배치 흐름 및 다른 박스와 관련하여 박스가 동작하는 방식이 달라진다.
        - outer display 타입
          - Block 타입: 하나의 독립된 덩어리처험 동작하는 요소
            - 항상 새로운 행으로 나뉜다(한 줄 전체를 차지한다. 너비 100%)
            - width, height, margin, padding 속성을 모두 사용할 수 있다.
            - padding, margin, border로 인해 다른 요소를 상자로부터 밀어낸다.
            - width 속성을 지정하지 않을 경우 박스는 inline 방향으로 사용 가능한 공간을 모두 차지한다. 
            - block 타입의 예시: h1~h6, p, div, ul, li
              - div: 다른 html 요소들을 그룹화하여 레이아웃을 구성하거나 스타일링을 적용할 수 있다. 헤더, 푸터, 사이드바 등 웹페이지의 다양한 섹션을 구조화하는데 가장 많이 쓰이는 요소이다.
          - Inline 타입: 문장 안의 단어처럼 흐름에 따라 자연스럽게 배치되는 요소
            - 줄바꿈이 일어나지 않는다.(즉, 컨텐츠의 크기만큼만 영역을 차지한다.)
            - width와 height 속성을 사용할 수 없다.
            - padding, margin, border가 적용되나, 수평방향으로만 다른 요소를 밀어낼 수 있다.
            - inline 타입의 예시: a, img, span, strong
              - span: 스타일을 적용하기 전에는 자체적으로 시각적 변화가 없고 텍스트의 일부를 조작하여 문장 내 특정 단어나 구문에만 스타일을 적용할 때 유용하다. 또한, 블록 요소처럼 줄바꿈을 일으키지 않으므로, 문서의 구조에 큰 변화를 주지 않는다.
          - normal flow: 일반적인 흐름 또는 레이아웃을 변경하지 않은 경우 웹페이지 요소가 배치되는 방식
          - inline-block: inline과 blcok의 특징을 모두 가진 특별한 display 속성 값. widith와 height 속성 사용이 가능하고, 다른 요소를 밀어낼 수 있다.
          - none: 요소를 화면에 표시하지 않고, 공간도 부여되지 않는다.
        - inner display 타입: 박스 내부의 요소들이 어떻게 배치될지를 결정한다.
          - CSS Flexobx(flex): 요소를 행과 열 형태로 배치하는 1차원 레이아웃
            - 구성요소
              - main axis
                - flex iteml들이 배치되는 기본 축
                - main start에서 시작하여 main end 방향으로 배치 (기본 값)
              - cross axis
                - main axis에 수직인 축
                - cross start에서 시작하여 cross end 방향으로 배치 (기본 값)
              - flex container
                - display: flex; 혹은 display:inline-flex; 가 설정된 부모 요소
                - 이 컨테이너의 1차 자식 요소들이 flex item이 된다.
                - flexbox 속성 값들을 사용하여 자식 요소 flex item들을 배치하는 주체이다.
              - flex item
                - flex container 내부에 레이아웃 되는 항목
                - 자유로운 순서 변경 및 정렬이 가능하다.
            - 속성 목록
              - flex container 관련
                - display
                  - display 속성을 flex로 설정하면 flex container로 지정할 수 있다.
                  - flex item은 기본적으로 행(주 축의 기본값)으로 나열된다.
                  - flex item은 주 축의 시작선에서 시작한다.
                  - flex item은 교차 축의 크기가 늘어나느 방향으로 늘어난다. 
                - flex-direction
                  - flex item이 나열되는 방향을 지정한다.
                  - 속성
                    - row(기본값): 아이템을 가로 방향으로 왼쪽에서 오른쪽으로 배치
                    - column: 아이템을 세로 방향으로 위에서 아래로 배치
                    - "-reverse"로 지정할 경우 아이템 배치의 시작 선과 끝 선이 서로 바뀐다.
                - flex-wrap
                  - flex item이 flex container의 한 행에 들어가지 않을 경우, 다른 행에 배치할지 여부 설정한다.
                  - 속성
                    - nowrap(기본값): 줄바꿈을 하지 않는다.
                    - wrap: 여러 줄에 걸쳐 배치될 수 있게 설정한다.
                - justify-content
                  - 주 축을 따라 flex item들을 정렬하고 간격을 조정
                  - 속성
                    - flex-start(기본값): 주 축의 시작점으로 정렬
                    - center: 주 축의 중앙으로 정렬
                    - flex-end: 주 축의 끝점으로 정렬
                - align-content
                  - 컨테이너의 여러 줄의 flex item이 있을 때, 그 줄들 사이의 공간을 어떻게 분배할지 지정
                  - flex-wrap이 wrap 또는 wrap-reverse로 설정된 여러 행에만 적용된다.
                  - flex 아이템이 두 줄 이상일 때만 의미가 있다.(flex-wrap이 nowrap으로 설정된 경우)
                  - 속성
                    - stretch(기본값): 여러 줄을 교차 축에 맞게 늘려 빈 공간을 채운다.
                    - center: 여러 줄을 교차 축의 중앙에 맞춰 정렬
                    - flex-start: 여러 줄을 교차 축의 시작점(보통 위쪽)에 맞춰 정렬
                    - flex-end: 여러 줄을 교차 축의 끝점(보통 아래쪽)에 맞춰 정렬
                - align-items
                  - 컨테이너 안에 있는 flex item들의 교차 축 정렬 방법을 지정
                  - 속성
                    - stretch(기본값): 아이템을 교차 축 높이를 꽉 채우도록 늘린다.
                    - center: 아이템을 교차 축의 중앙에 맞춰 정렬한다.
                    - flex-start: 아이템을 교차 축의 시작점에 맞춰 정렬
                    - flex-end: 아이템을 교차 축의 끝점에 맞춰 정렬
              - flex item 관련
                - align-self
                  - 컨테이너 안에 있는 flex item들을 교차 축을 따라 개별적으로 정렬
                  - 속성
                    - auto
                    - stretch
                    - center
                    - flex-start
                    - flex-end
                - flex-grow
                  - 남는 행 여백을 비율에 따라 각 flex item에 분배
                  - flex item이 컨테이너 내에서 확장하는 비율을 지정한다.
                - flex-basis
                  - flex item의 초기 크기 값을 지정한다.
                  - flex-basis와 width 값을 동시에 적용한 경우 flex-basis를 우선한다.
                - order
  - CSS Position
    - 요소를 normal flow에서 제거하여 다른 위치로 배치하는 것. 요소를 다른 요소 위에 올리거나 화면의 특정 위치에 고정할 수 있다.
      - position 속성: 네가지 방향 속성을 이용해 요소의 위치를 조절할 수 있고 겹치는 요소의 쌓이는 순서를 조절할 수 있다.
        - static(기본 값)
          - 요소를 normal flow에 따라 배치.
          - top, right, bottom, left 속성이 적용되지 않는다.
        - relative 
          - 요소를 normal flow에 따라 배치하되 자신의 원래 위치(static)를 기준으로 top, right, bottom, left 속성으로 위치를 조정할 수 있다. 
          - 다른 요소의 레이아웃에는 영향을 주지 않는다.
        - absolute
          - 요소를 normal flow에서 제거. 
          - 가장 가까운 relative 부모 요소를 기준으로 이동한다. (만족하는 부모 요소가 없을 경우, body 태그를 기준으로 한다.) 
          - top, right, bottom, left 속성으로 위치를 조정할 수 있다. 
          - 문서에서 요소가 차지하는 공간이 없어진다.
        - fixed
          - 요소를 normal flow에서 제거.
          - 현재 화면영역(viewport)을 기준으로 이동한다.
          - 스크롤해도 항상 같은 위치에 유지된다.
          - top, right, bottom, left 속성으로 위치 조정이 가능하다.
          - 문서에서 요소가 차지하는 공간이 없어진다.
        - sticky
          - relative와 fixed의 특성을 결합한 속성
          - 스크롤 위치가 임계점에 도달하기 전에는 relative처럼 동작하다가 스크롤 위치가 임계점에 도달하면 fixed처럼 화면에 고전된다.
          - 다음 sticky 요소가 나올 경우 이전 sticky 요소의 자리를 대체한다. (두 sticky의 요소의 위치가 겹치게 되기 때문에.)
      - z-index: 요소의 쌓임 순서를 정의하는 속성. 높을 수록 위에 쌓인다.
        - static이 아닌 요소에만 적용된다.
        - 기본값은 auto로 부모 요소의 z-index 값에 영향을 받는다.
        - 같은 부모 내에서만 z-index값을 비교하고, 값이 같으면 html 문서 순서대로 쌓인다.
        - 자식의 z-index가 아무리 높아도 부모보다 위로 올라갈 수 없다.
  - Bootstrap: CSS 프론트렌트 프레임워크(toolkit). 미리 만들어진 다양한 디자인 요소들을 제공하여 웹사이트를 빠르고 쉽게 개발할수 있도록 한다.
    - CDN(Content Delivery Network): 서버와 사용자 사이의 물리적인 거리를 줄여 콘첸츠 로딩에 소요되는 시간을 최소화하는 방식. 지리적으로 사용자와 가까운  CDN 서버에 콘텐츠를 저장해서 사용자에게 전달한다.
    - 기본 사용법: Bootstrap에는 특정한 규칙이 있는 클래스 이름으로 스타일 및 레이아웃이 미리 작성되어 있다.
      - 예시(spacing을 표현하는 방법: {property}{sides}-{size})
        - property: margin 또는 padding
          - m, p
        - sides: 방향(top, bottom, left, right, (top, bottom), (left, right), 4 sides)
          - t, b, s, e, y, x, blank
        - size: spacing의 상대적 너비
          - 1 = 0.25 rem = 4px
          - (0, 0 rem, 0px), (2, 0.5 rem, 8px), (3, 1 rem, 16px), (4, 1.5 rem, 24px), (5, 3 rem, 48px)
          - auto
        ```html
        <p class="mt-5">Hello, world!</p>
        ```
    - Reset CSS: 모든 html 요소 스타일(element, table, lise 등)을 일관된 기준으로 재설정하는 간결하고 압축된 규칙 시트
      - 모든 브라우저는 각자의 user agent styleheet를 갖고 있고 이것이 브라우저마다 다르기 때문에 모든 브라우저에서 웹사이트가 동일하게 보이게 하기 위해 같은 스타일 상태로 만드는 과정이다.
      - Normalize CSS: Reset CSS 방법 중 대표적인 방법으로 웹 표준 기준으로 브라우저 중 하나가 불일치한다면 차이가 있는 브라우저를 수정하는 방법이다.
      - bootstrap의 경우 bootstrap-reboot.css하는 파일명으로 normalize.css를 자체적으로 커스텀해서 사용하고 있다.
    - Typography
      - display headings ```class="display-1~6```: 기존 headings보다 더 눈에 띄는 제목이 필요할 경우 사용한다.
      - inline text elements
        - 하이라이트 ```<mark></mark>```
        - 굵은 취소선 ```<del></del>```
        - 취소선 ```<s></s>```
        - 밑줄 ```<ins></ins>```
        - 밑줄2 ```<u></u>```
        - small, strong, em, ... etc
      - lists
    - Colors
      - bootstrap color system: bootstrap이 지정하고 제공하는 색상 시스템으로 일관성 있는 의미론적 관점의 색상을 적용할 수 있게 해준다.
    - Bootstrap Component: bootstrap에서 제공하는 ui 관련 요소. 일관된 디자인을 제공하여 웹사이트의 구성 요소를 구축하는데 유용하게 활용할 수 있다.
    - 참조: CDN 없이 bootstrap 사용하기
      - 1. bootstrap 코드 파일 다운로드 (https://getbootstrap.com/docs/5.3/getting-started/download/)
      - 2. bootstrap.css와 bootstrap.bundle.js만 선택
      - 3. css 파일은 html head 태그에 가져와서 사용
      - 4. js 파일은 html body 태그에 가져와서 사용
- Semantic web: 웹데이터를 의미론적으로 구조화된 형태로 표현하는 방식으로 외형보다는 요소 자체의 의미에 집중하는 것에 가깝다.
  - HTML Semantic Element: 기본적인 모양과 기능 이외의 의미를 가지는 HTML 요소
    - header: 소개 및 탐색에 도움을 주는 콘텐츠
    - nav: 현재 페이지 내, 또는 다른 페이지로의 링크를 보여주는 구획
    - main: 문서의 주요 콘텐츠
    - article: 독립적으로 구분해 배포하거나, 배포될 수 있는 구성의 콘텐츠 구획
    - section: 문서의 독립적인 구획. 더 적합한 요소가 없을 때 사용한다.
    - aside: 문서의 주요 내용과 간접적으로만 연관된 부분
    - footer: 가장 가까운 조상 구획(main, article 등)의 작성자, 저작권 정보, 관련 문서
  - CSS 방법론: CSS를 효율적이고 유지보수가 용이하게 작성하기 위한 일련의 가이드라인
    - OOCSS(Object-Oriented CSS): 객체 지향적 접근법을 적용하여 CSS를 구성하는 방법론
      - 1. 구조와 스킨의 분리함으로써 가독성을 높인다.        
      - 2. 컨테이너와 콘텐츠의 분리
        - 객체에 직접 적용하는 대신 객체를 둘러싸는 컨테이너에 스타일을 적용한다.
        - 스타일을 정의할때 위치에 의존적인 스타일을 사용하지 않도록 한다.
        - 콘텐츠를 다른 컨테이너로 이동시키거나 재배치할 때 스타일이 깨지는 것을 방지한다.
- 반응형 웹 디자인(Responsive Web Design): 디바이스 종류나 화면 크기에 상관없이, 어디서든 일관된 레이아웃 및 사용자 경험을 제공하는 디자인 기술
  - Bootstrap Grid System: 웹 페이지의 레이아웃을 조정하는 데 사용되는 12개의 column과 6개의 breakpoint로 구성된 시스템
    - 구조
      - container: column을 담고 있는 공간
      - column: 실제 콘텐츠를 포함하는 부분
        - 1개의 row 안에 12개의 column 영역이 구성된다.
        - 기본: ```class:col-n```으로 n개의 column을 할당. ```class:col```로 균등 분배 가능.
        - 중첩(nesting): row 안에 row를 설정 가능.
        - 상쇄(offset): ```class: col-n offset-m```으로 m개의 column을 생략 가능.
      - gutter: column 간의 여백 영역(상하좌우)
        - x축은 padding, y축은 margin을 여백 생성
        - padding을 사용 할 때, 실제 컬럼 간의 좌우 간격이 변하는 것이 아닌 content의 너비가 변하는
      - grid system breakpoints: 웹페이지를 다양한 화면 크기에서 적절하게 배치하기 위한 분기점. 화면 너비에 따하 6개의 분기점(xs,sm,md,lg,xl,xxl)이 제공된다.
        - 기본값: (xs < 576px <= sm < 768px <= md < 992px <= lg < 1200px <= xl < 1400px <= xxl> )
        - 각 breakpoints 마다 설정된 최대 너비값 **이상**으로 화면이 커지면 grid system 동작이 변경된다.
        - ```<div class="col-size-n">```: 화면 크기가 size 이상일경우 col-n을 할당
        - ```<div class="offset-size-m">```: offset도 column과 마찬가지로 사이즈별 할당이 가능하다.
- 사용자(User)
  - UX(User Experience): 제품이나 서비스를 사용하는 사람들이 느끼는 전체적인 경험과 만족도를 개선하고 최적화하기 위한 디자인과 개발 분야
    - 사람들의 마음과 생각을 이해하고 정리해서 제품에 녹여내는 과정
    - 유저 리서치, 데이터 설계 및 정제, 유저 시나리오, 프로토타입 설계
  - UI(User Interface): 서비스와 사용자 간의 상호작용을 가능하게 하는 디자인 요소들을 개발하고 구현하는 분야
    - 예쁜 디자인보다는 사용자가 더 쉽게 편리하게 사용할 수 있도록 고려하기
    - 디자인 시스템, 중간 산출물, 프로토타입 등의 관리가 필요하다.

---

Django
-
웹 애플리케이션(web application) 개발
- 인터넷을 통해 사용자에게 제공되는 소프트웨어 프로그램을 구축하는 과정
- 다양한 디바이스에서 웹 브라우저를 통해 접근하고 사용할 수 있다.

클라이언트와 서버
- client: 서비스를 요청하는 주체. 사용자의 웹 브라우저, 모바일 앱
- server: 클라이언트의 요청에 응답하는 주체

프론트엔드와 백엔드
- 프론트엔드: 사용자 인터페이스를 구성하고, 사용자가 애플리케이션과 상호작용할 수 있도록 한다.
  - HTML, CSS, JavaScript, 프론트엔드 프레임워크 등.
- 백엔드: 서버 측에서 동작하며, 클라이언트의 요청에 대한 처리와 데이터베이스와의 상호작용 등을 담당.
  - 서버 언어(python, java 등) 및 백엔드 프레임워크, 데이터베이스, api, 보안 등

웹 프레임워크
- 웹 애플리케이션을 빠르게 개발할 수 있도록 도와주는 도구

Django: 파이썬 기반의 대표적인 웹 프레임워크
  - 학습 목적: 클라이언트 - 서버 구조에서의 서버를 구현하기

가상 환경: 하나의 컴퓨터 안에서 또 다른 독립된 파이썬 환경을 구축하는 것.
- 여러개의 프로젝트를 진행할 때, 각 프로젝트가 한 패키지에 대해 다른 버전을 요구할 경우 독립적인 개발 환경이 요구된다.
- 각각 다른 프로젝트에서 사용하고 있는 패키지 a와 패키지 b가 있고 두 패키지를 동시에 사용시 충돌 위험이 있을 때 독립적인 개발 환경이 필요하다.
- ``` $ python -m venv venv ``` 가상 환경 생성
  - 현재 디렉토리 안에 venv라는 이름의 가상 환경 폴더를 생성.
  - venv 폴더 안에는 파이썬 실행 파일, 라이브러리 등을 담을 공간이 마련된다.
  - 임의의 이름으로 생성이 가능하나 관례적으로 venv를 사용.
- ``` $ source venv/Scripts/activate ``` 가상 환경 활성화
- ``` $ deactivate ``` 가상 환경 종료

의존성(dependency): 하나의 소프트웨어가 동작하기 위해 필요로 하는 다른 소프트웨어나 라이브러리
의존성 패키지: 프로젝트가 의존하는 개별 라이브러리들을 일컫는 말. 즉, 프로젝트가 실행되기 위해 꼭 필요한 각각의 패키지.
패키지 목록 확인: ``` $ pip list```
의존성 기록: ``` pip freeze ``` > requirements.txt
- 가상 환경에 설치된 모든 패키지를 버전과 함께 특정한 형식으로 출력.
- 이를 txt 파일로 저장하면 나중에 동일한 환경을 재현할 때 유용하다.
- 협업 시에도 팀원들이 똑같은 버전의 라이브러리를 설치하도록 공유 가능
- txt 파일의 이름은 requirements를 사용하는 것이 관례
- 협업시 venv 파일이 아닌 의존성 기록 txt파일을 공유하여 버전을 동기화한다.
가상 환경 사용 시 주의사항
- 가상 환경에 들어가고 나오는 것이 아니라 사용할 파이썬 환경을 on/off로 전환하는 개념
  - 가상 환경 활성화는현재 터미널 환경에만 영향을 끼친다. 새 터미널 창을 열면 다시 활성화해야 한다.
  - 프로젝트마다 별도의 가상환경을 사용해야 한다.
  - 일반적으로 가상 환경 폴더 venv는 관련된 프로젝트와 동일한 경로에 위치시켜야 한다.
  - 폴더 venv는 .gitignore 파일에 작성하여 원격 저장소에 공유하지 않도록 한다.
    - venv 폴더 용량이 크기 때문에 저장소 크기를 줄이기 위해서
    - OS별 차이점으로 인한 문제를 방지
    - 이를 위해 requirements.txt를 공유

쟝고 프로젝트 디자인 패턴
- 디자인 패턴: 소프트웨어 설계에서 반복적으로 발생하는 문제에 대한, 검증되고 재사용 가능한 일반적인 해결책. 대표적인 디자인 패턴으로는 MVC가 있다.
- MVC 디자인 패턴: 하나의 애플리케이션을 구조화하는 대표적인 구조적 디자인 패턴
  - Model: 데이터 및 비즈니스 로직을 처리
  - View: 사용자에게 보이는 화면을 담당
  - Controller: 사용자의 입력을 받아 model과 view를 제어.
  - 시각적 요소와 뒤에서 실행되는 로직을 서로 영향 없이, 독립적으로 쉽게 유지보수할 수 있는 애플리케이션을 만들기 위함.
- MTV 디자인 패턴: django에서 애플리케이션을 구조화하는 디자인 패턴
  - 기존 MVC 패턴과 동일하나 view -> template, controller -> view로 명칭을 다르게 정의한 것.

프로젝트와 앱
- django project: 애플리케이션의 집합
  - db 설정, url 연결, 전체 앱 설정 등을 처리
- django application: 독립적으로 작동하는 기능 단위 모듈
  - 각자 특정한 기능을 담당
  - 다른 앱들과 함께 하나의 프로젝트를 수어
- 앱 생성하기
  - 1. ``` $ python manage.py startapp appnames ```
    - 앱의 이름은 복수형으로 지정할 것을 권장
  - 2. 앱 등록: 반드시 앱을 생성한 후 등록해야 한다.
    - settings.py의 INSTALLED_APPS에 지정한 앱 이름을 문자열로 추가하기
- 프로젝트 구조
  - 자주 수정할 파일
    - settings.py: 프로젝트의 모든 설정을 관리
    - urls.py: 요청이 들어오는 url에 따라 이에 해당하는 적절한  views를 연결
  - 학습 과정에서 수정할 일 없는 파일
    - \_\_init__.py: 해당 폴더를 패키지로 인식하도록 설정하는 파일
    - asgi.py: 비동기식 웹 서버와의 연결 관련 설정
    - wsgi.py: 웹 서버와의 연결 관련 설정
    - manage.py: django 프로젝트와 다양한 방법으로 상호작용하는 커맨드라인 유틸리티
- 앱 구조
  - 자주 수정할 파일
    - admin.py: 관리자용 페이지 설정
    - models.py: DB와 관련된 model을 정의 (MTV 패턴의 M)
    - views.py: http 요청을 처리하고 해당 요청에 대한 응답을 반환 (MTV 패턴의 V)
      -  url, model, template과 연동
 - 수정할 일 없는 파일
   - apps.py: 앱의 정보가 작성된 곳
   - tests.py: 프로젝트 테스트 코드를 작성하는 곳 
요청과 응답: 사용자가 서버에 접속하는 과정
- 1. URLs
- 2. View: 특정 경로에 있는 tempalte과 request 객체를 결합해 응답 객체를 반환
- 3. Template: 앱 폴더 안에 templates 폴더를 **직접** 생성하고 templates 폴더 안에 앱이름 폴더를 만든다.

데이터 흐름에 따른 코드 작성하기
- 사용자의 요청에서부터 데이터의 흐름은 URLs -> View -> Template
- 코드의 작성도 이 흐름을 따라 이루어져야 한다.

django tempalte system
- 파이썬 데이터(context)를 HTML 문서(template)과 결합하여, 로직과 표현을 분리한 채 동적인 웹페이지를 생성하는 도구
- 페이지 틀에 데이터를 동적으로 결합하여 수많은 페이지를 효율적으로 만들어내기 위해 사용된다.

```html
<body>
  <h1>Hello, Django!</h1>
</body>
```
'django!' 부분을 변수로 바꾸기
->
```python
# views.py
def index(request):
    context = {
        'name': 'Jane',
    }
    return render(request, 'articles/index.html', context)
```
```html
<body>
  <h1>Hello, {{ name }}!</h1>
</body>
```
django template language(DTL): tempalte에서 조건, 반복, 변수 등의 프로그래밍적 기능을 제공하는 시스템
  - variable
    - django template에서의 변수
    - render 함수의 세번재 인자로, 딕셔너리 타입으로 전달된다.
    - 해당 딕셔너리 key에 해당하는 문자열이 template에서 사용 가능한 변수명이 된다.
    - dot('.')을 사용하여 변수 속성에 접근이 가능하다.
    - ``` {{ variable }} ```
    - ``` {{ variable.attribute }}```
  - filters
    - 표시할 변수를 수정할 때 사용(변수 + '|' + 필터)
    - chained(연결)가 가능하며 일부 필터는 인자를 받기도 한다.
    - 약 60개의 built-in tempalte filters를 제공하고 있다.
    - ``` {{ variable|filter }} ```
    - ``` {{ name|truncatewords:30 }} ```
  - tags
    - 반복 또는 논리를 수행하여 제어 흐름을 만든다.
    - 일부 태그는 시작과 종료 태그가 필요하다.
    - 약 24개의 built-in tempalte tags를 제공하고 있다.
    - ``` {% tag %} ```
    - ``` {% if %} {% endif %} ```
  - comments(주석)
    - inline: ``` <h1>Hello, {# name #}</h1> ```
    - multiline: ``` {% comment %} ... {% endcomment %} ```
템플릿 상속
- 페이지의 공통 요소를 포함
- 하위 템플릿이 재정의 할 수 있는 공간을 정의
- 여러 템플릿이 공통된 요소를 공유할 수 있게 해주는 기능
- 상속 구조 만들기
  - skeleton 역할을 하게 될 상위 템플릿 html을 작성
  - 템플릿이 공유할 공통요소를 작성.
  - 템플릿 별로 재정의가 필요한 부분은 blcok 태그를 활용한다.
  - 하위 템플릿은 extend 태그를 통해 상속받을 템플릿을 결정
  - 하위 템플릿에도 block 태그를 사용해 상위 템플릿에 작성된 block 태그의 영역을 대체

요청과 응답: 데이터를 보내고 가져오기
- html 'form' 요소를 통해 사용자와 애플리케이션 간의 상호작용이 이루어진다.
- 핵심 속성
  - action: 입력 데이터가 전송될 URL을 지정(목적지)
  - method: 데이터를 어떤 방식으로 보낼 것인지 정의. 데이터의 http request method(GET, POST)를 지정
- HTTP request 객체: form으로 전송한 데이터 뿐 아니라 django로 들어오는 모든 요청 관련 데이터가 담겨 있다.
- django URLs
  - URL dispatcher(운항 관리자, 분배기)
  - variable routing: URL 일부에 변수를 포함시키는 것
  - app URL mapping: 각 앱에 URL을 정의하는 것
    - 프로젝트 내부의 urls.py에 모든 url이 담겨 있는 것을 각 앱의 urls.py에서 각자의 url을 관리하게끔 구조를 수정
    - include('app.urls'): 프로젝트 내부 앱들의 url을 참조할 수 있도록 매핑하는 함수
  - URL 이름 지정
    - naming url patterns: url에 이름을 지정하는 것
      - path 함수에 name 인자를 키워드 인자로 정의해서 사용한다.
    - DTL url tag ```{% url 'url_name' arg1 arg2 %}: 주어진 url 패턴의 이름과 일치하는 절대 경로 주소를 반환한다.
  - URL 이름 공간
    - 서로 다른 앱의 url 이름이 같을 경우 이름에 key 를 붙인다.
    - urls.py에 app_name 변수를 설정해야 한다.
- form tag vs routing