
## Chapter 1

- 딕셔너리가 있는데 굳이 name tuple을 사용하는 이유가 뭘까?


---
## Chapter 3: Dictionary and Set

-  왜 불변 속성을 가지는 객체들만 hash 가능할까?

>  hash 를 사용하는 주요한 목적 중 하나는 hash table을 만들어서 검색을 용이하게 하기 위함임.
>  하지만 hash 하고자 하는 가변 가능할 경우, table 상의 key 값과 불일치 하게 되기 때문에 객체 수명주기동안 동일하게 유지되는 것이 보장되어야 함


- 왜 딕셔너리에 저장된 값들은 "원칙적으로" 순서 정보를 포함 할 수 없는가?

> 이는 dict 클래스에서 키들을 해쉬 테이블에 저장하는 순서와 관련있다. 다음의 예시를 한번 살펴보자
> dict01 = {key01: value01, key02: value02}, dict02 = {key02: value02, key01: value01}
> 만약 key01과 key02의 해쉬값이 충돌할 경우, 다음의 과정을 겪게된다
> (dict01의 경우)
> 1. key01을 hash table에 저장 (이 위치를 id01 이라 하자)
> 2. key02를 hash table에 저장하려 시도
> 3. hash 충돌 감지 후, 다르게 hash. (이 위치를 id02 이라 하자)
> (dict02의 경우)
> 4. key02을 hash table에 저장 (id01)
> 5. key01를 hash table에 저장하려 시도
> 6. hash 충돌 감지 후, 다르게 hash. (id02)
> 결과적으로 dict01과 dict02는 동일한 dict로 분류되어야 함에도 불구하고 hash 테이블 상에서 다른 순서를 가지게 됨. -> 순서 정보가 의미가 없어야 함!


---
## Chapter 4: Text and Bytes



---
## Chapter 7: Function decorator and Closure

- 데코레이터는 왜 특이한 사용 문법을 가지고 있음?
> 함수 데코레이터는 본질적으로 syntatic sugar임. 예시를 통해 설명해드림
```python
@decorate
def target(args):
    return None
```
> 구문은 본질적으로 다음과 같음
```python
target = decorate(target)
```
> 사용의 편의성을 위해서 함수의 정의 단계에서 데코레이터 구문을 적용할 수 있게 했을 뿐, 익숙한 형태로 언제든 변환 가능함

- import time 과 run time 의 차이가 뭐임?
> 파이썬 파일을 실행하면 코드의 종류에 따라서 실행되는 시간이 나뉨. import time 에는 import 구문과 데코레이터 코드가 실행됨. run time 에는 나머지 코드가 실행됨. @registry 구문 같은 데코레이터를 사용해보면 그 차이를 극명하게 볼 수 있음. 

- 데코레이터 문법 사용 예시
	- 내부 함수 없음 (제일 단순)
	- 내부 함수 1중 -> 일반적으로 가장 많이 사용하는 방식
	- 내부 함수 2중 -> 데코레이터에 매개변수를 넣고 싶을 때. 데코레이터 팩토리 ( 데코레이터 ( 실제 함수 ) ) 형태


---
## Chapter 8. Object referencing, Mutability, Recyling
- '=' 연산자와 'is' 연산자의 차이?
	- '=' 연산자는 객체의 '값'을 비교
	- 'is' 연산자는 객체의 정체성 (객체가 저장된 id)를 비교

- 일반적 할당 (등호), copy.copy (얕은 복사), copy.deepcopy (깊은 복사) 차이가 뭐임?
	![[Pasted image 20250612133742.png]]
>	보면 알 수 있지만, 할당은 id가 안 변함. 얕은 복사는 객체는 새롭게 생성하지만 내부 객체들은 공유함. 깊은 복사는 내부 객체들까지 아예 새롭게 생성함. 


- 최소 놀람의 법칙? principle of least surprise
> 코드의 작동방식이 사용자의 기대와 최대한 일치해야 한다는 원칙. 당연한 말 같지만, 어떤 인터페이스를 디자인 할 때, 그 인터페이스의 기대 되는 사용자들이 친숙한 방식으로 디자인해야 한다는 실용적 의미로 해석되곤 함. 예를 들어서 마이크로소프트 윈도우 프로그램을 개발한다면, 윈도우의 기본 단축어들을 지원해야함. 이런 식으로 사용됨. 

- 가변 매개변수 관련 팁
	- __절대로 가변형을 매개변수 기본값으로 사용하지 말 것!__
		![[Pasted image 20250612140943.png]]
		이런 대참사가 일어남

	- __가변 매개변수를 인수로 받을 시 함수 내부에서 새롭게 객체를 생성해서 사용할 것__
		최소 놀람의 원칙에 부합함

---
## Chap 9: Pythonic Objects
- repr 과 str 메서드의 차이가 뭐임?
> __repr__: 객체의 문자열을 개발자가 보고 싶은 형태로 반환 -> 일반적으로 해당 객체를 생성하기 위한 코드
> __str__ : 객체의 문자열을 사용자가 보고 싶은 형태로 반환

- 일반적 method, @classmethod, @staticmethod 차이가 뭐임?
	![[Pasted image 20250612144356.png]]
	들어가는 인수가 다름!
	- 일반 method: self (생성된 인스턴스 자신)가 첫번째 인수로 들어감
	- classmethod: 클래스가 첫번째 인수로 들어감
	- staticmethod: 암것도 안들어감. 일반 함수처럼 이용가능

---
## Chap 10: Sequence Hacking, Hash, Slice
- 덕 타이핑 (duck typing) 이 뭐임?
> 특정 객체 사용하기 위해서 적절한 객체인지를 검사할 때, 정확한 클래스를 검사하기보다는 원하는 작동 메서드를 가지고 있는지 검사하는 방법. "오리인지 검사하지 말고, 오리처럼 걷고, 오리처럼 꽥꽥 대는지를 검사해라 (알렉스 마르텔리)" 라는 말에서 유래했음
	![[Pasted image 20250612152036.png]]

---
## Chap 15. Context Manager and Else Block

- __EAFP__
	- Easier to Ask Forgiveness than Permission
	- 용서를 구하는 것이 허락을 구하는 것보다 쉽다
	- 타입 검사를 하지 않고, 일단 실행을 해보고 오류가 나면 이후 예외 처리를 진행하는 방식.
	- 파이썬에서 권장하는 에러 처리 흐름
- __LBYL__
	- Leap Before You Leap
	- 누울 자리를 보고 발을 뻗어라
	- 일단 타입 검사를 먼저 진행 한 뒤에, 일치하는 경우에만 이후 코드를 진행하는 방식
	- 예시
```python
# EAFP style
try:
    value = mapping[key]
except:
	print("there's no keys in your dictionary.")
else:
	return value

# LBYL style
if key in mapping:
    return mapping[key]
else:
	print("there's no keys in your dictionary.")
```

- __contextlib.contextmanager__
	- with 구문을 사용하기 위한 클래스 사용을 간편화한 문법.
	- __enter__, __exit__ 메서드를 yield 전후로 나눠서 구현하면 됨
```python
def looking_glass():
	def reversed_text(text):
	    return text[::-1]
	original_stdout = sys.stdout.write
	reversed_stdout = reversed_text(original_stdout)
	sys.stdout.write = reversed_stdout

	try:
	    yield 'JABBERWOCKY' # 여기 이전까지 __enter__ 시 시행
	except ZeroDivisionError:
	    print("Please Do Not Divice by Zero!") # 에러 처리
	finally:
	    sys.stdout.write = original_stdout # 여기부터 __exit__ 시행
	    if msg:
	        print(msg)
```

---
## Chap 16. Coroutine
- __coroutine__
	- 정의: 일반적으로 "서브루틴"(일반적 함수) 과정은 "호출→실행→리턴 "의 단방향 단계로 이뤄짐. 코루틴은 __중간에 실행을 멈출 수 있거나__, __필요할 때, 중단 시점에서 다시 시작할 수 있으며__, __호출자와 값을 주고 받을 수도 있음__. 즉, 협력적(ConCurrent) 으로 시행될 수 있는 과정을 의미함
	- 예시: __제너레이터 기반 문법__ -> yield 키워드를 활용하여 중단 지점 설정 가능