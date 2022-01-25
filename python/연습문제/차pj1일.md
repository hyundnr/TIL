## We love kriii

> ACM-ICPC 인터넷 예선, Regional, 그리고 World Finals까지 이미 2회씩 진출해버린 kriii는 미련을 버리지 못하고 왠지 모르게 올해에도 파주 World Finals 준비 캠프에 참여했다.
>
> 대회를 뜰 줄 모르는 지박령 kriii를 위해서 격려의 문구를 출력해주자.

```python
print('강한친구 대한육군\n강한친구 대한육군')
```



## 고양이		=>		여기부터 다시~ 안해!

> 아래 예제와 같이 고양이를 출력하시오.

```python
a = "\    /\"
b =  ")  ( ')"
c = "(  /  )"
d = "\(__)|" 
print(f'{a}\n{b}\n{c}\n{d}')
```



## A+B

```python
두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

a, b = map(int, input().split())
print(a + b)
```



## A-B

```python
a, b = map(int, input().split())
print(a - b)
```

## 사칙연산

```python
a, b = map(int, input().split())
print(a + b)
print(a - b)
print(a * b)
print(a // b)
print(a % b)
```

## ??!

>  준하는 사이트에 회원가입을 하다가 joonas라는 아이디가 이미 존재하는 것을 보고 놀랐다. 준하는 놀람을 ??!로 표현한다. 준하가 가입하려고 하는 사이트에 이미 존재하는 아이디가 주어졌을 때, 놀람을 표현하는 프로그램을 작성하시오.

```python
a = input()
print(f'{a}??!')
```

## 1998년생인 내가 태국에서는 2541년생?!

> ICPC Bangkok Regional에 참가하기 위해 수완나품 국제공항에 막 도착한 팀 레드시프트 일행은 눈을 믿을 수 없었다. 공항의 대형 스크린에 올해가 2562년이라고 적혀 있던 것이었다.
>
> 불교 국가인 태국은 불멸기원(佛滅紀元), 즉 석가모니가 열반한 해를 기준으로 연도를 세는 불기를 사용한다. 반면, 우리나라는 서기 연도를 사용하고 있다. 불기 연도가 주어질 때 이를 서기 연도로 바꿔 주는 프로그램을 작성하시오.

```python
y = int(input())
print(y - 543)
```



## 나머지

> (A+B)%C는 ((A%C) + (B%C))%C 와 같을까?
>
> (A×B)%C는 ((A%C) × (B%C))%C 와 같을까?
>
> 세 수 A, B, C가 주어졌을 때, 위의 네 가지 값을 구하는 프로그램을 작성하시오.

```python
A, B, C = map(int, input().split())
print((A + B) % C)
print(((A % C) + (B % C)) % C)
print((A * B) % C)
print(((A % C) * (B % C)) % C)
```



## 곱셈

> (세 자리 수) × (세 자리 수)는 다음과 같은 과정을 통하여 이루어진다.
>
> ![img](%EC%B0%A8pj1%EC%9D%BC.assets/f5NhGHVLM4Ix74DtJrwfC97KepPl27s%20(1).png)
>
> (1)과 (2)위치에 들어갈 세 자리 자연수가 주어질 때 (3), (4), (5), (6)위치에 들어갈 값을 구하는 프로그램을 작성하시오.

```python
a = str(input())
b = str(input())    
for i in reversed(b):
    print(int(a) * int(i))
print(int(a) * int(b))
```

