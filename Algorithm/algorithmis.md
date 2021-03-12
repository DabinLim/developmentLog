# 알고리즘이란 

- 문제 해결을 위하여, 입력된 자료를 토대로 원하는 출력을 유도해내는 규칙의 집합이다.
- 여러 단계의 유한 집합으로 구성되는데, 각 단계는 하나 또는 그 이상의 연산을 필요로 한다.

<br>

## 알고리즘을 공부하는 이유

- 좋은 프로그램을 구현하는 개발자가 되기 위하여
- 좋은 프로그램을 만들기 위해서는 특정 자료구조나 접근방법이 필요하다.
- 즉, 여러 자료구조와 방법들을 배우고 익혀야 좋은 프로그램을 만들 수 있다..

- 그렇다면, 좋은 프로그램이란? <br>
적은 공간을 이용하여 빠른 속도로 수행되는 프로그램<br><br>

## 시간 복잡도 개념

- 입력값과 문제를 해결하는데 걸리는 시간과의 상관관계
- 입력값이 늘어나도 필요한 공간이 덜 늘어나는 알고리즘이 효율적인 알고리즘이다.
- 각 줄이 실행 되는 걸 1번의 연산이 된다고 생각하고 계산한다.

```
array = [3, 5, 6, 1, 2, 4]

for i in array:             # len(array) 만큼 아래 연산 실행
        for j in array:     # len(array) 만큼 아래 연산 실행
            if i < j:       # 비교 연산 1번 실행
                break
        else:
            return l
```
> 위 코드는 이중 for문을 이용하여 배열의 최댓값을 구하는 코드이다.<br><br>
배열 array의 길이만큼 for문이 실행되었고 for문이 한번 돌때마다 for문 안의 이중for문으로 배열 array 만큼의 연산 더 실행된다<br><br>
2번째 for문 안에서는 i 와 j의 값을 비교하는 연산이 1번 실행된다.<br><br>
위의 연산을 더해보면 N(입력값) * N(입력값) * 비교연산1 번의 연산을 하였다.<br><br>
그러므로 위의 코드는 N^2 만큼의 시간이 걸렸다고 표현한다.


### N의 길이에 따른 연산량

| N의 길이 |N^2 | 2N + 1 
|------|----------|---------|
| 1 | 1 | 3
| 10 | 100 |21
| 100 | 10000 |201
| 1000 | 1000000 |2001
| 10000 | 100000000 |20001

<br>

- N의 지수가 커질수록 입력값이 높아짐에 따라 걸리는 시간이 크게 늘어난다.<br>
따라서 상수는 신경쓰지 말고, N의 지수에 따라 점근 표기법으로 표기한다.<br>
<br>

## 공간 복잡도 개념

- 입력값과 문제를 해결하는데 필요한 공간과의 상관관게를 말한다.
- 시간 복잡도와 마찬가지로 입력값이 늘어나도 필요한 공간이 덜 늘어나는 알고리즘이 효율적인 알고리즘이다.

```
 array = [3, 5, 6, 1, 2, 4] # 6개의 공간을 사용


def find_max_num(array):
    max_num = array[0]        # 1개의 공간을 사용
    for num in array:      
        if num > max_num:  
            max_num = num     
    return max_num

```
> 위의 코드는 7개의 공간을 사용하였다고 표현할 수 있다.<br><br>
공간복잡도의 경우 사용된 공간이 상수일 경우가 많아 대부분의 경우 알고리즘의 성능이 공간에 의해서 결정되지 않는다.

<br><br>

## 점근 표기법

- 알고리즘의 성능을 수학적으로 표기하는 방법으로 효율성을 평가하는 방법이다.
- 점근 표기법의 종류로는 빅오 (Big-O) 표기법과 빅 오메가 (Big-Ω) 표기법이 있다.<br>
* 빅오 표기법은 '최악'의 성능이 나올 때의 연산량, 빅 오메가 표기법은 '최선'의 성능이 나올 때의 연산량을 표기한다.
- 입력값이 최선의 경우일 가능성은 매우 낮으며, 최악의 경우에 대비하기 위해 거의 모든 알고리즘은 빅오 표기법으로 분석한다.

> 입력값이 좋을때 연산량이 1이고 안 좋을 때 연산량이 N일 경우 <br><br>
빅오 표기법 = O(N)<br><br>
빅 오메가 표기법 = Ω(1)