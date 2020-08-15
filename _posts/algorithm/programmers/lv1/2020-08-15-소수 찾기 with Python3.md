---
layout: post
title: (LV1) 소수 찾기 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

## Lv1. 연습문제 - 소수 찾기

<br>

![](https://i.imgur.com/M04S5LB.png)

<br>

> 이 문제는 에라토스테네스의 체라는 방식을 사용해야 한다.
>
> 작은 개수의 소수를 구하는 데는 우리가 흔히 알고 있는 소수의 정의를 사용해 풀어도 되지만 위와 같은 문제처럼 다수의 소수를 한꺼번에 찾는 문제는 에라토스테네스의 체를 사용하는 것이 훨씬 효율적이다.

<br>

```shell
일반 소수 구하기 알고리즘 시간복잡도 : O(N)
에라토스테네스의 체 시간복잡도 : O(nloglogn)
```



<br>

---

#### 에라토스테네스의 체 방식은

> 2의 배수를 지우고, 3의 배수를 지우고, ... n/2 의 배수를 지우고..
>
> 즉, **소수가 아닌 것들을 지워가며 소수인 것만 남기는 방법**이라 할 수 있다.
>
> ⋇ **n의 제곱근 전의 정수들 (int(sqrt(n)))** 까지만 loop를 돌며 걸러내도 모든 소수가 아닌 것들이 걸러지는데, 필자의 경우 기억하기 쉽게 n/2로 기억해두었다.

---



<br>

소스코드는 다음과 같다.

```python
def solution(n):
    # True : 소수, False : 소수x
    check = [True] * (n+1)
    check[0] = check[1] = False
    for i in range(2, (n//2)+1):
        if not check[i] :
            continue
        for j in range(2*i, n+1, i):
            if check[j] :
                check[j] = False
    return check.count(True)
```



<br>

<br>

[소수 찾기 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/소수%20찾기.py)

<br>