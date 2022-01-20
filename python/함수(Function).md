## 함수(Function)

- 특정한 기능을 하는 `코드의 조각(묶음)`
- 필요 시에만 호출하여 간편히 사용
- `for문`을 함수로 추출해 반복 사용한다고 생각



### 사용자 함수(Custom Fincton)

- 구현되어 있는 함수가 없는 경우 사용자가 직접 함수 작성 가능

```python
def function_name(parameter):
    return
```

[ex]

```python
def foo():			#<= 선언 
    return True

#호출시
 foo()
```



## 실습 문제

> 입력 받은 수를 세제곱하여 반환하는 함수 cube 를 작성하시오
>
> 함수 cube를 활용하여 2의 세제곱, 100의 세제곱을 구하시오

```python
def cube(number):
    return number * number * number

print(cube(2), cube(100))
```



## return VS print

- `return` 은 함수 안에서만 사용되는 `키워드`
- `print` 는 출력을 위해 사용되는 `함수`



## 함수의 결과값(Output)

- `return`이 없으면 => None 반환
- `return`이 있으면 => 하나(객체)를 반환



## 실습문제

> 너비와 높이를 입력받아 사각형의 넓이와 둘레를 튜플로 반환하는 함수 rectangle을 작성하시오.

```python
def rectangle(width, height):
    return width * height, (width + height) * 2


```



## 함수의 입력(Input)

- Argument
  - 함수 호출 시 함수의 parameter를 통해 전달되는 값
  - 소괄호 안에 할당 func_name(argument)
- Positional Arguments
  - 기본적으로 함수 호출 시 Argument는 위치에 따라 함수 내에 전달 됨
- Keyword Arguments
  - 직접 변수의 이름으로 특정 Argument를 전달 할 수 있음



## 정리

### 함수

- 로직을 분해하는것 / 추상화 => 기본적으로 위치 기반 (`호출`/ `정의`)
- **Input **
- **Output**  =>  반드시 하나의 객체 반환

- 호출  =>  위치 / 키워드
- 정의  =>  필수 / 선택 / 많을때는 `*`( tuple) **or** `**` (dictionary) 사용



- 함수는 블랙박스다 !  => LEGB 를 이용해 값을 찾아감...
- 값을 바꿀 수 있는 키워드는 **global**, **nonlocal**  => 함부로 사용은 ㄴㄴ 





## 함수 호출

1. **정의된 순서대로 값을 넘겨준다.**

   ```python
   add(1, 2)
   ```

2. **정의된 이름(파라미터)를 키워드로 해서 하나씩 넘겨준다.**

   ```python
   add(x=1, y=2)
   ```

   

## 함수 정의

1. 아무 것도 안하기

```python
def add(x,y):
    pass
```

2. 기본 값 설정 (호출하는 입장에서 해당 파라미터는 선택적으로 쓸 것)

```python
def add(x, y=0):
    pass
```

3. 정의되지 않은 갯수

​	 1. 나열(시퀀스)

```python
def add(*arge):
    pass
	# 내부에서 args 튜플로 동작
```

​	 2. Key-Value

```python
def func(**kargs):
    pass
```



```python
def foo(a, b, c=1):
    # 기본 값? 선택적으로 값을 넘기라
    pass

foo(c=1)
```

