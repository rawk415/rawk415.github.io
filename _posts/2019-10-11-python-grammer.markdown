---
layout: post
title: "Python 문법"
subtitle: "python"
categories: devlog
tags: python
---
## 세미콜론 `;`
세미콜론은 보통 찍지 않는다.   
```python
print('Hello world!')
print('1234')
  

print('Hello world!'); print('1234')
```   

위 아래 문장은 동일하며 보통 한 줄에 여러 구문을 사용할 땐 세미콜론으로 구분한다.   

---


## 주석 `#`
주석은 리눅스와 동일한 #이다.   
여타 주석과 동일하게 # 뒤의 코드는 읽지 않는다.   

```python
# 파이썬 주석
print('Hello world!') # 안녕 세상
```  

---

## 들여쓰기 `Tab`
파이썬에서는 중괄호`{ }`를 사용하지 않는다. 따라서 들여쓰기를 하지 않으면 오류가 발생한다.   
들여쓰기를 하면 자동으로 괄호와 같은 효과를 지닌다.   
들여쓰기는 공백(space) 4칸을 표준으로 한다.

```python
if a ==10:
print('문법오류')

if a == 10:
    print('a=10 입니다.')
    print('들여쓰기는 동일하게!')
```

---

## 연산
- 더하기 `+`
- 빼기 `-`
- 곱하기 `*`
- 나누기 `/`
- 몫 구하기(소수점 버림) `//`
- 나머지 연산 `%`
- 거듭 제곱 연산 `**`
- 행렬 곱셈 연산 `@`

```python
# 행렬 곱셈 연산
# pip install numpy. (numpy 모듈 설치)
import numpy ad np
a = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
b = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]]) 
a @ b

# array([[ 30,  36,  42],
#        [ 66,  81,  96],
#        [102, 126, 150]])
```

---

## 비교 연산
- 크다 `>`
- 작다 `<`
- 크거나 같다 `>=`
- 작거나 같다 `<=`
- 같다(값) `==`
- 다르다(값) `!=`
- 같다(객체) `is`
- 다르다(객체) `is not`

---

## 정수로 값 받기 `int()`
나눗셈을 할 경우 결과가 무조건 실수가 나온다.   
이를 정수형으로 받으려면 int()로 감싸면 된다.    
정수로 된 문자열도 정수형으로 반환할 수 있다.(Integer.parseInt와 동일)   

```python
4/2 
# 2.0

int(4/2) 
# 2

int('10') 
# 10
```   

---

## 실로로 값 받기 `float()`
`int()`와 동일하게 `float()`안의 결과를 실수로 반환한다.   
정수, 실수, 정수 or 실수로 된 문자열이 가능하다.

```python
float(0) 
# 0.0

float('10.3') 
# 10.3
```

---

## 자료형 알아내기 `type()`
`type()` 함수를 이용하면 자료형을 알 수 있다.

```python
type('10')
# <class 'str'>

type(10)
# <class 'int'>

type(4/2)
# <class 'float'>
```

---

## 객체의 주소 알아내기 `id()`
`id()` 함수를 이용하면 객체의 주소를 알 수 있다.

```python
a = 1
id(a); id(1)
# 1540187312

a = 10
id(a); id(10)
id(10.0)
# 1540187456
# 64057328
```

---

## 몫과 나머지 구하기 `divmod()`
`divmod()`를 사용하면 몫과 나머지가 튜플(tuple) 형태로 동시에 나온다.

```python
divmod(4, 2)
# (2, 0)

quotient, remainder = divmod(4, 2)
# quotient = 2, remainder = 0
```

---

## 변수 

### 변수 할당 `=`
여타 언어들과 같이 `=`을 통해 변수를 할당한다.
```python
x, y, z = 10, 3.14, 'PI'
# x = 10, y = 3.14 z = 'PI'

x = y = z = 10
# x = 10, y = 10, z = 10


x, y = 10, 20
x, y = y, x
# x = 20, y = 10
# temp 변수 없이 값의 교환이 이뤄진다.
```

### 변수 삭제 `del x`
파이썬은 특이하게 변수를 삭제하는 기능을 제공한다.

```python
x = 10
del x
```

### 공간만 할당(값 할당 x) `None`
null로 대표되는 변수 공간만 만드는 값은 파이썬에서는 `None`을 사용한다.

```python
x = None
```

---

## 입력하기 `input()`
C언어의 `scanf()`, JAVA의 `Scanner`와 동일한 기능을 하는 입력 값을 받아오는 메소드는 `input()` 이다. 괄호() 안에는 어떤 입력 값인지를 명시적으로 출력해 줄 값을 넣을 수 있다.  
C에서 `scanf()`를 쓰기 전에 `printf()`로 어떤 값인지 출력해주는 것을 동시에 할 수 있다.
변수에 저장되는 타입은 모두 문자열인 `String` 타입이다.

```python
a = input('Num1 : ')
print(a)

# 결과
# Num1 : (입력 값)
# ('입력 값')
```

### 여러 값 입력받기 `.split()`
`input()`만을 사용하면 한 번에 하나의 값만 입력 받을 수 있다.    
한 번에 여러 값을 입력 받기 위해서는 `input()`의 매서드인 `split()`을 사용한다.   
`split()`의 인자에는 여러 값을 구분할 구분 문자를 입력하고, Default값은 공백이다. 

```python
a, b, c = input('입력 값: ').split(^)
# 입력 값: 10^20.5^'Hello'
# a = 10, b = 20.5, c = 'Hello'
```

### 숫자형 타입으로 저장

#### 하나의 입력 값을 저장할 때 `int(input())`
`input()`을 `int()`로 감싸서 입력값을 int()로 반환한다.

```python
a = int(input())
type(a)
# <class 'int'>
```

#### 여러개의 입력 값을 저장할 때 `map()`
`map`을 사용해 split의 결과를 숫자형 타입으로 변환할 수 있다.

```python
a, b = map(float, input('입력 값: ').split(','))
# 입력 값: 12.5,13
# a = 12.5, b = 13.0
type(a) type(b)
# <class 'float'>
```

---

## 출력하기 `print()`
`print()`에 인자값을 넣으면 출력된다.   
`,`로 구분 시 공백으로 띄워지고 그 뒤에 한줄로 출력된다.   

```python
print(1, 2, 3, 'Hello', 'python')
# 1 2 3 Hello python
```

### 여러 줄 문자열`""" """`
`print()`의 인자를 따옴표`' '` 하나로 감싸지 않고 3개로`''' '''` 감싸면 `print()`문을 여러 번 쓰지 않고 여러 줄에 걸쳐 출력할 수 있다.

```python
print('''hi
my name is
python''')

# hi
# my name is
# python
```

### 값 사이 문자 지정 `sep=''`
`print()`의 마지막 인자에 `sep=''`을 넣어줌으로써 인자들을 구분하는 문자를 지정할 수 있다.   
`sep=''`에 escape문자들(`\n` `\t` `\r` 등)도 넣어줄 수 있다.


```python
print(5, 2, 7, sep='x')
# 5x2x7

print(5, 2, 7 sep='\t')
# 5     2       7
```

### 뒤에 이어서 출력 `end=''`
`print()`의 인자에 `end=''`를 넣어주면 다음 `print()`까지 이어 한 줄에 출력할 수 있다.   
`end=''` 에 넣는 값에 따라 print문들을 연결하는 문자를 지정할 수 있다.

```python
print('Hello', end='123')
print('python', end='\t')
print(1, 2, 3)

# Hello123python    1 2 3
```



















