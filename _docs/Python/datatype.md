---
title: 데이터 타입
category : Python
order: 5
layout: default
comments: true
---
작성자 : 김준성 2017-03-16

## 데이터타입이란?
파이썬으로 a 라는 변수에 10을 넣는다고 할 때 ```a=10```이런식으로 코드를 작성한다. 그리고 name 이라는 변수에 Junseong Kim을 넣을때 ```name="Junseong Kim"```이런식으로 작성을 한다. 그런데, 딱봐도 a에는 숫자가 들어가있고, name에는 문자가 들어갔다는 것을 직관적으로 알 수 있다.

컴퓨터도 이를 인식 한다. a변수에다가 숫자를 넣으면, a의 데이터 타입은 숫자가 된다. 그리고 name변수에다가 ""안에 문자를 넣으면 name변수의 데이터타입은 문자열가 된다. 즉 **이 데이터의 특성이 무엇인가? 이게 바로 데이터 타입이다.**

좀더 간단한 예제로, 메이플 스토리 캐릭터를 짠다고 하자. HP, MP는 숫자. 캐릭터 이름과 길드명은 문자열라고 당연하게 생각 할 수 있다.
```python
name = "타락파워전사" #name은 문자열
level = 10 #level은 숫자
HP = 9999 #HP는 숫자
MP = 1234 #MP는 숫자
club_name = "소융메플길드"  #club_name은 문자열
```

대표적인 변수타입으로는 아래와 같은 내용이 있다
- Int (정수)
- Float (소수)
- String (문자열)
- Boolean (참,거짓)

## Int : 정수 타입

```python
a=10
```
라는 코드는 a에 10을 넣은것이다. 10은 정수이기 때문에, a의 데이터 타입은 정수(Integer)가 된다. 근데 프로그래밍에서는 **정수를 보통 Int라고 한다.** 그래서 a의 데이터 타입은 Int이다.

```python
print(int(3.14))  #결과는 3이 출력됨
```
int()함수로 묶어 주게 되면 안에 있는 값이 정수로 변환된다. 위와 같은 경우에는 3.14라는 소수를 정수로 바꿔준 결과가 나타난 것이다.

## Float : 소수 타입

```python
pi = 3.14
```
라는 코드는 pi에 3.14를 넣은것이다. 3.14는 소수이기 때문에, pi의 데이터 타입은 소수(Float)이 된다. 프로그래밍에서도 역시 **소수를 보통 float이라고 한다.** 그래서 pi의 데이터 타입은 Float 이다.

```python
print(float(3)) #결과 3.0이 출력됨
```
float()함수로 묶어주게 되면 안에 있는 값이 소수로 변환된다. 위와 같은 경우에는 정수 3을 소수로 바꿔서 3.0이 출력되는 결과가 나타나는 것이다.


## String : 문자열
```python
school_name = "국민대학교"
```
라는 코드는 school_name에 국민대학교 라는 값을 넣은 것이다. 변수에 문자열을 넣을때는 ""큰 따움표로 감싸서 넣어야 한다(중요!).

아! 왜 문자가 아니라, 문자열이라고 하나면 **문자는 한글자, 문자열은 여러글자** 로 사용된다. 간단하다. 예를 들어서 아래와 같은 코드를 생각 할 수 있다.
```python
a='a'   # a는 문자
name ="Junseong" #name은 문자열
```

자 여기서 재밌는 생각을 해볼 수 있다. 아래와 같은 코드를 생각해보자.
```python
nickname = "Superwarrior126"
password = "1234"
pi = "3.14"
```
nickname에 문자열과 숫자가 섞여있다. 그럼 nickname은 문자열인가 숫자인가? **무조건 ""로 묶여있는 것은 무조건 문자열이다.** 더욱 놀라운 것은 password의 데이터 타입 또한 int(정수)가 아니다. 문자열이다. ""로 묶여 있기 때문이다. 그리고 pi 역시 문자열이다.

그럼 pi를 소수로 바꿔주고 싶다! 이럴때는 float()함수를 써서 소수로 바꿔주면 된다. 그리고 password도 정수로 바꿔주고 싶다, 이럴땐 int()함수를 써서 정수로 바꿔주면된다.

```python
# 문자열 -> 숫자로
pi = float("3.14") # 결과는 3.14(소수)
password = int("1234") #결과는 1234(정수)

# 숫자 -> 문자열
pi = str(3.14) # 결과는 "3.14"(문자열)
password = str(1234) #결과는 "1234"(문자열)
```

그리고 **문자나 다른 타입의 변수를 문자열로 바꿀때는 str()함수를 이용하면 된다.**

## Boolean : 참,거짓

얘는 조금 쉽다. 한마디로 참과 거짓을 갖는 데이터 타입이다.

```python
korean_love_kimchi = True #한국인은 김치를 좋아합니다 : 참
i_am_KMU_Student = True #전 국민대 학생입니다 : 참

i_am_SNU_Student = False #전 서울대 학생입니다 : 거짓
have_boyfriend = False # 남자친구가 있습니다 : 거짓(?)
```
즉 True라는 값과 False라는 값만 넣을 수 있다. 나중에 비교연산자와 if문에서 조금 더 심화적으로 다루어 볼 예정이다.

#### 비교연산자

```python
== 같다
!= 같지 않다
> 왼쪽이 크다
< 오른쪽이 크다
>= 왼쪽이 더 크거나 같다
<= 오른쪽이 더 크거나 같다
```

위에처럼 있는데 아래처럼 사용한다
```python
is_equal = (1234 == 1234) # True (1234와 1234가 같다 : 참)
is_big = (1 < 999) # True (999가 1보다 크다 : 참)

is_small = (1 > 999) # False (999가 1보다 작다 : 거짓)
isnt_same = (1 != 1) # False (1과 1은 같다. 따라서 1과 1이 다르냐 라는 질문은 거짓이다.)
```

뭐 좀더 실생활에서는 이렇게 사용된다. 조건문은 나중에 알려줄게요...
```python
id = "junseong123"
pw = "js0217"

#만약 id가 junseong123이고 pw가 js0217이면 로그인 아니면 로그인 실패
if id == "junseong123" and pw == "js0217":
  print("로그인 성공!!")
else:
  print("로그인 실패!!")
```

## 데이터 타입 알아보기
```python
a = "Junseong" # 문자열
print(type(a)) # <class 'str'> 문자열 타입 str이라고 인식한다

b = 10
print(type(b)) # <class 'int'> 정수 타입 int라고 인식한다

c = 1.1123
print(type(c)) # <class 'float'> 소수타입 float라고 인식한다

d = True
print(type(d)) # <class 'bool'> bool타입 bool이라고 인식한다
```
type()이라는 함수를 이용해서 타입을 알아 낼 수 있다.