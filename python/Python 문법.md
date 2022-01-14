## Python 문법 (date : 22'. 01. 14)

### 대/소문자

### 띄어쓰기

### 스펠링



###  저장 (할당)

- 박스에 값을 담는거라고 생각

1. 숫자

2. 글자

   `따옴표`로 들어감

   '58'은 글자

3. 참/거짓

   True, False 두가지

- 어떻게 저장하는가 => 리스트(List)=>박스 여러개

  ```python
  dust = [58, 40, 70]
  print(dust[1])
  =>40
  
  #합치기 가능!!
  lunch = ['닭가슴살', '피자', '계란']
  dinner_box = ['청양고추맛 닭가슴살', '바베큐맛 닭가슴살']
  meal_box = [lunch, dinner_box]
  print(meal_box)
  [['닭가슴살', '피자', '계란'], ['청양고추맛 닭가슴살', '바베큐맛 닭가슴살']]
  ```

- 딕셔너리(dictionary)=>견출지 붙인 박스

```python
dust = {'영등포구':40, '강남구':50}
dust['영등포구']
=>40


phone_book = {'A': '010-1234-5678', 'B': '010-9876-5432', 'C': '010-4567-8901'}

print(phone_book)
print(phone_book['A'])
```



##  Type 확인

> 변수 타입 확인

```python
a = 'hello'
print(type(a))
<class 'str'>
```



## 조건

> if, elif, else

```python
dust = 100

if 150 < dust:
    print('매우 나쁨')
# elif dust > 80 and dust <= 150: 으로 써도 됨!!
elif 80 < dust < 150:
    print('나쁨')
elif 30 < dust < 80:
    print('보통')
else:
    print('좋음')

=>나쁨

# 이하 조건 없어도 잘 돌아감
dust = 100

if 150 < dust:
    print('매우 나쁨')
elif 80 < dust:
    print('나쁨')
elif 30 < dust:
    print('보통')
else:
    print('좋음')

=>나쁨
```



## 반복

> while, for

- `while`은 `해당하는 조건`일 동안 계속 반복 => 종료조건 필요
- `for`는 `정해진 범위`안에서 반복 => 종료조건 필요X

```python
greeting = "Guten Tag!!"

#while 문

i = 0
while i < 10:
    print(greeting)
    i = i + 1

#for 문

for i in range(10):
    print(greeting)

=>Guten Tag!!
Guten Tag!!
Guten Tag!!
Guten Tag!!
Guten Tag!!
Guten Tag!!
Guten Tag!!
Guten Tag!!
Guten Tag!!
Guten Tag!!
```

### 교수님꺼

```python
greeting = 'Guten Tag!!!!!'

# while문? 
# 10번 실행하고 싶어. 
# 0부터 9까지 올라가면서 10되면 종료하도록?
i = 0 
while i < 10: # 해당 조건이 False가 되면, 종료!
    print(greeting)
    i = i + 1

# for문? 
# 10번 실행하고 싶어.
# 통 : range(10)
print(range(10))

for i in range(10):
    # i = _________
    print(i)

lunch_box = ["kfc", "버거킹", "맥도날드"]
# 런치박스의 내용을 하나씩 menu에 넣어줌.
for menu in lunch_box:
    # menu = 
    print(menu)

# 런치박스의 길이(len) 만큼 숫자들을 나열시키고 (range)
# 하나씩 i에 인덱스를 넣어줌
for i in range(len(lunch_box)):
    # 인덱스에 하나씩 접근
    print(lunch_box[i])
```



## 함수

> 반복 작업을 위해 사용

- 어떠한 `input`을 받아서 `logic`을 사용해 `output`을 반환

```python
def dust_quality(dust):
    if 150 < dust:
        print('매우 나쁨')
    elif 80 < dust < 150:
        print('나쁨')
    elif 30 < dust < 80:
        print('보통')
    else:
        print('좋음')
    return

dust_quality(100)
dust_quality(30)
dust_quality(600)

=>나쁨
좋음     
매우 나쁨
```

## 모듈

```python
# 1. 모듈 불러오기
import random

# 2. 점심 메뉴 리스트를 만들고
lunch_box = ['닭가슴살', '피자', '계란']

# 3. 하나를 랜덤으로(random) 선택하여(choice) 저장한다.
today_menu = random.choice(lunch_box)
# 4. 출력한다.
print(today_menu)

=> 피자
```

- 로또 번호 만들기

```python
# 1. 모듈 불러오기
import random
# 2. 숫자 통(1~45)
numbers = range (1, 46)     # range(n,m) => n이상 m미만
# 3. 그 중에서 6개 sample
ture_numbers = random.sample(numbers, 6)
# 4. 그 결과를 출력
print(ture_numbers)

=>[18, 13, 9, 40, 42, 5]

# 같은 코드
import random
print(random.sample(range(1, 46), 6))
```

