## A+B - 5

> 두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

```python
#True인 동안 실행
while 1:   
    A, B = map(int, input().split())
	if A == 0 and B == 0:
        break
    else:
        print(A + B)
    
```



## A+B - 4

> ## 예제 입력 1 복사
>
> ```
> 1 1
> 2 3
> 3 4
> 9 8
> 5 2
> ```
>
> ## 예제 출력 1 복사
>
> ```
> 2
> 5
> 7
> 17
> 7
> ```

```python
while 1:
    # 인풋 갯수가 정해지지 않았기 때문에 예외처리 사용!
    try:
	    a, b = map(int, input().split())
	    print(a + b)
    except:
        break
```



## 더하기 사이클 =>다시

> 0보다 크거나 같고, 99보다 작거나 같은 정수가 주어질 때 다음과 같은 연산을 할 수 있다. 먼저 주어진 수가 10보다 작다면 앞에 0을 붙여 두 자리 수로 만들고, 각 자리의 숫자를 더한다. 그 다음, 주어진 수의 가장 오른쪽 자리 수와 앞에서 구한 합의 가장 오른쪽 자리 수를 이어 붙이면 새로운 수를 만들 수 있다. 다음 예를 보자.
>
> 26부터 시작한다. 2+6 = 8이다. 새로운 수는 68이다. 6+8 = 14이다. 새로운 수는 84이다. 8+4 = 12이다. 새로운 수는 42이다. 4+2 = 6이다. 새로운 수는 26이다.
>
> 위의 예는 4번만에 원래 수로 돌아올 수 있다. 따라서 26의 사이클의 길이는 4이다.
>
> N이 주어졌을 때, N의 사이클의 길이를 구하는 프로그램을 작성하시오.

```python
num = int(input())
initial = copy.num
count = 0
while 1:
    if num < 10:
    	a = 0
        b = num
        num = b * 10 + (a + b)
        count += 1
    	if num == initial:
        	break
            print(count)
        
    else:
        a = num // 10
        b = num % 10
        num = b * 10 + (a + b)
        count += 1
        if num == initial:
        	break
            print(count)
```



## 최소, 최대

> 첫째 줄에 주어진 정수 N개의 최솟값과 최댓값을 공백으로 구분해 출력한다.

```python
T = int(input())
numbers = list(map(int, input().split()))
max = numbers[0]
min = numbers[0]
for number in numbers:
    if number > max:
        max = number
    elif number < min:
        min = number
print(min, max)
```



## 최댓값

> 9개의 서로 다른 자연수가 주어질 때, 이들 중 최댓값을 찾고 그 최댓값이 몇 번째 수인지를 구하는 프로그램을 작성하시오.
>
> 예를 들어, 서로 다른 9개의 자연수
>
> 3, 29, 38, 12, 57, 74, 40, 85, 61
>
> 이 주어지면, 이들 중 최댓값은 85이고, 이 값은 8번째 수이다.

```python
total_list = []
for i in range(9):
    total_list.append(int(input()))
print(max(total_list))
print(total_list.index(max(total_list)) + 1)
```



## 숫자의 개수

> 세 개의 자연수 A, B, C가 주어질 때 A × B × C를 계산한 결과에 0부터 9까지 각각의 숫자가 몇 번씩 쓰였는지를 구하는 프로그램을 작성하시오.
>
> 예를 들어 A = 150, B = 266, C = 427 이라면 A × B × C = 150 × 266 × 427 = 17037300 이 되고, 계산한 결과 17037300 에는 0이 3번, 1이 1번, 3이 2번, 7이 2번 쓰였다.

```python
```

