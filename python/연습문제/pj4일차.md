# 숫자의 개수

> 세 개의 자연수 A, B, C가 주어질 때 A × B × C를 계산한 결과에 0부터 9까지 각각의 숫자가 몇 번씩 쓰였는지를 구하는 프로그램을 작성하시오.
>
> 예를 들어 A = 150, B = 266, C = 427 이라면 A × B × C = 150 × 266 × 427 = 17037300 이 되고, 계산한 결과 17037300 에는 0이 3번, 1이 1번, 3이 2번, 7이 2번 쓰였다.

```python
A = int(input())
B = int(input())
C = int(input())
calculated_number = str(A * B * C)
for i in range(10):
    count = 0
    for j in range(len(calculated_number)):
        if str(i) == calculated_number[j]:
            count += 1
    print(count)
```



## 나머지 

> ## 문제
>
> 두 자연수 A와 B가 있을 때, A%B는 A를 B로 나눈 나머지 이다. 예를 들어, 7, 14, 27, 38을 3으로 나눈 나머지는 1, 2, 0, 2이다. 
>
> 수 10개를 입력받은 뒤, 이를 42로 나눈 나머지를 구한다. 그 다음 서로 다른 값이 몇 개 있는지 출력하는 프로그램을 작성하시오.

```python
A =int(input())
B =int(input())
C =int(input())
D =int(input())
E =int(input())
F =int(input())
G =int(input())
H =int(input())
I =int(input())
J =int(input())
result = []
result.append(A % 42)
result.append(B % 42)
result.append(C % 42)
result.append(D % 42)
result.append(E % 42)
result.append(F % 42)
result.append(G % 42)
result.append(H % 42)
result.append(I % 42)
result.append(J % 42)
print(len(set(result)))
```



## 평균 

> 세준이는 기말고사를 망쳤다. 세준이는 점수를 조작해서 집에 가져가기로 했다. 일단 세준이는 자기 점수 중에 최댓값을 골랐다. 이 값을 M이라고 한다. 그리고 나서 모든 점수를 점수/M*100으로 고쳤다.
>
> 예를 들어, 세준이의 최고점이 70이고, 수학점수가 50이었으면 수학점수는 50/70*100이 되어 71.43점이 된다.
>
> 세준이의 성적을 위의 방법대로 새로 계산했을 때, 새로운 평균을 구하는 프로그램을 작성하시오.

```python
T = int(input())
input_list = list(map(int, input().split()))
total = 0
for i in input_list:
   total += (i / max(input_list)) * 100
print(total / T)
```



## OX퀴즈

> "OOXXOXXOOO"와 같은 OX퀴즈의 결과가 있다. O는 문제를 맞은 것이고, X는 문제를 틀린 것이다. 문제를 맞은 경우 그 문제의 점수는 그 문제까지 연속된 O의 개수가 된다. 예를 들어, 10번 문제의 점수는 3이 된다.
>
> "OOXXOXXOOO"의 점수는 1+2+0+0+1+0+0+1+2+3 = 10점이다.
>
> OX퀴즈의 결과가 주어졌을 때, 점수를 구하는 프로그램을 작성하시오.

```python
T = int(input())
for i in range(1, T + 1):
    total_score = 0
    OX = str(input())
    score = 0
    for num in range(len(OX)):
        if OX[num] == 'O':
            score += 1
            total_score += score
        else:
            score = 0
    print(total_score)
```



## 평균은 넘겠지

> ## 문제
>
> 대학생 새내기들의 90%는 자신이 반에서 평균은 넘는다고 생각한다. 당신은 그들에게 슬픈 진실을 알려줘야 한다.

```python
T = int(input())
for i in range(1, T + 1):
    score_list = list(map(int, input().split()))
    students_number = score_list.pop(0)
    average = sum(score_list) / students_number
    count = 0
    for score in score_list:
        if score > average:
            count += 1
    portion = round((count * 100 / students_number), 3)
    print(f'{portion:0.3f}%')
```

