---
layout: post
title: (LV1) 정수 제곱근 판별 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---



## Lv1. 연습문제 - 정수 제곱근 판별

<br>



![](https://i.imgur.com/rXDhhjz.png)

<br>

> 1. math의 sqrt를 이용해 제곱근을 구한 후 제곱근을 int로 변환한 것과 비교!
>
>    > 파이썬의 sqrt함수는 float형 return이지만, 소수점 뒤가 0일 경우 int형과 비교해주었을 때 같은 것으로 취급! Ex) 12.0 = 12
>
> 2. 다르다면 -1 return

<br>

소스코드는 다음과 같다.

```python
import math
def solution(n):
    return int(math.sqrt(n)+1) ** 2 if math.sqrt(n) == int(math.sqrt(n)) else -1
```



<br>

<br>

[정수 제곱근 판별 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/정수%20제곱근%20판별.py)