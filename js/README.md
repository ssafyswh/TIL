DOM(Document Object Model): 웹페이지(document)를 구조화된 객체로 제공하여 프로그래밍 언어가 페이지 구조에 접근할 수 있는 방법을 제공.
DOM API: 다른 프로그래밍 언어가 웹페이지에 접근 및 조작할수 있도록 페이지 요소들을 객체 형태로 제공하며 관련 메서드도 함께 제공한다.
- document 객체: 웹페이지를 나타내는 DOM 트리의 최상위 객체. HTML문서의 모든 콘텐츠에 접근하고 조작할 수 있는 진입점이 된다.
- DOM에서 모든 요소, 속성, 텍스트는 하나의 객체이며, document 객체의 하위 객체로 구성된다.
- DOM tree: html 태그를 나타내는 요소들의 node는 문서의 구조를 결정한다. 이들은 다시 자식 노드를 가질 수 있다. (객체 간 상속 구조가 존재한다)
- 웹페이지를 동적으로 만들기 == 웹페이지를 조작하기
  - 조작하고자 하는 요소를 선택(혹은 탐색)하고 선택된 요소의 콘텐츠 또는 속성을 조작한다.
  - 선택 메서드
    - document.querySelector(selector)
      - 제공한 선택자와 일치하는 첫번째 요소를 한개 선택한다.
      - 제공한 선택자를 만족하는 첫번째 요소 객체를 반환한다. (없다면 null을 반환)
    - document.querySelectorAll(selector)
      - 제공한 선택자와 일치하는 여러 요소를 선택한다.
      - 제공한 선택자를 만족하는 nodelist를 반환한다.
  - 조작 메서드
    - 속성 조작
      - 클래스 속성(classList property) 조작 메서드: 요소의 클래스 목록을 DOMTokenList(유사 배열) 형태로 반환
        - element.classList.add(): 지정한 클래스 값을 추가
        - element.classList.remove(): 지정한 클래스 값을 제거
        - element.classList.toggle(): 클래스가 존재한다면 제거하고 false를 반환(존재하지 않으면 클래스를 추가하고 True를 반환)
      - 일반 속성 조작 메서드
        - Element.getAttribute(): 해당 요소에 지정된 값을 반환
        - Element.setAttribute(): 지정된 요소의 속성 값을 설정. 속성이 이미 있다면 기존 값을 갱신한다.
        - Element.removeAttribute(): 요소에서 지정된 이름을 가진 속성을 제거한다.
      - HTML 콘텐츠 조작
      - DOM 요소 조작 메서드
        - document.createElement(tagName): 작성한 tagname의 html 요소를 생성하여 반환
        - Node.appendChild(): 한 노드를 특정 부모 노드의 자식 노드리스트 중 마지막 자식으로 삽입 후 추가된 Node 객체를 반환한다.
        - Node.removeChild(): DOM에서 자식 노드를 제거 후 제거된 노드를 반환.
  - DOM 용어 정리
    - Node: DOM의 기본 구성 단위
    - NodeList: DOM 메서드를 사용해 선택한 Node의 목록
    - Element: DOM 트리에서 HTML 요소를 나타내는 특별한 유형의 Node
    - Parsing: 브라우저가 문자열을 해석하여 DOM Tree로 만드는 과정(구문 분석, 해석)
    - var: ES6 이전에 변수 선언에 사용했던 키워드
      - 함수 스코프(function scope): 함수의 중괄호 내부를 가리키고, 함수 스코프를 갖는 변수는 함수 바깥에서 접근할 수 없다.
      - 호이스팅(hoisting): 변수 선언문이 코드의 최상단으로 끌어올려지는 듯한 현상. var로 선언된 변수는 선언 위치와 관계없이 스코프 최상단에서 선언된 것처럼 동작하며, 할당 전가지는 undefined 값을 갖는다.
        - 허강사님 부가설명: **런타임 이전에** 선언문이 코드의 최상단으로 끌어올려지는 듯한 현상.
        - ```var a = 1;```: ```var a;```라는 변수선언문과 ```a = 1;```라는 변수할당문이 합쳐진 코드.

데이터 타입
- 원시 자료형(primitive type): 값(value) 자체가 변수에 직접 저장되는 자료형. 불변(immutable)이며, 변수 할당 시 값이 복사된다.
  - Number: 정수 또는 실수형 숫자를 표현하는 자료형
    - 문자열과 + 연산시, 숫자가 문자열로 자동 형 변환되어 연결된다.
    - 정수와 실수 구분이 없고, 모든 숫자를 단일 타입으로 처리한다.
  - String: 텍스트 데이터
    - template lieterals( like f-string in python): 내장된 표현식을 허용하는 향상된 문자열 작성 방식 `${ }` 
  - null: 프로그래머가 의도적으로 값이 없음을 표현
  - undefined: 시스템이나 js 엔진이 값이 할당되지 않음을 나타낼 때 사용
  - boolean: 참과 거짓을 나타내는 논리적인 자료형(true, false)
- 참조 자료형(reference type): 데이터가 저장된 메모리의 주소가 변수에 저장되는 자료형. 가변(mutable)이며, 변수 간 할당 시 주소가 복사된다. Objects(object, array, function)

연산자
- 할당 연산자(=)
- 증가 / 감소 연산자(++, --)
- 비교 연산자
- 동등 연산자(==)
  - 두 피연산자가 같은 값으로 평가되는지 비교한 후 불리언 값 반환
  - 암묵적 타입 변환을 통해 타입을 일치시킨 후 값을 비교한다.
  - 두 피연산가 모두 객체일 경우, 메모리의 같은 객체를 바라보는지 판별
- 일치 연산자(===)
  - 두 피연산자의 값과 티입이 모두 같은 경우 참을 반환
  - 엄격한 비교가 이루어지며, 암묵적 타입변환이 발생하지 않는다.
- 논리 연산자
  - and(&&)
  - or(||)
  - not(!)

조건문
- if
- 삼항 연산자": condition ? expression1(true) : expression2(false)

반복문
- while
- for
- for in: object 순회
- for of: iterable 순회

함수
- 참조 자료형에 속하며 모든 함수는 function object
