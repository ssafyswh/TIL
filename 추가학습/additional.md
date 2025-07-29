객체지향(Object-Oriented Programming, OOP)
-
- 객체: 현실 세계의 사물이나 개념을 코드로 표현한 것

class: 전체 구조를 저장할 무언가(설계도)
객체: 실제 데이터를 저장한 무언가

class Smartphone:
	# 초기화하는 함수
    # 매직 메서드: 언더바 2개로 감싸져 있는 매서드
    # 파이썬 내부에서 특별한 상황에 자동으로 호출된다.
	def __init__(self, model, price):
		self.model = model
		self.price = price

giryunPhone = Smartphone('wide5', '0원')
beomseokPhone = Smartphone('galaxy 21', '100만원')

\* 파이썬이 __init__이라는 함수를 호출하도록 만들어 놨기 때문에 가능한 일! 

해싱(hasing): 값을 해시 함수를 통해 정수로 변환 후 버킷에 저장하는 것?
해시 값(정수)이 너무 클 경우 ```return hash_value % bucket_size```를 통해 버킷 내 저장 위치를 조정
다른 값을 해싱했을 때, 이미 값이 저장된 위치의 해시 값이 나왔을 경우 해시 충돌
일반적으로 해시 충돌 발생시 그 다음 위치에 저장한다.
  - 해시 충돌: 다른 key 값이 서로 같은 해시 값을 갖는 경우. 
  - 딕셔너리는 그럴 일 없다! 왜?
버킷이 가득 찼을 경우 bucket size를 2배로 늘린다.