---
layout: post
title: (LV1) 최대공약수와 최소공배수 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

<br>

## Lv1. 연습문제 - 최대공약수와 최소공배수

<br>



![](https://i.imgur.com/aH7pd2e.png)

<br>

> math 라이브러리의 gcd(n,m) 함수를 이용해 쉽게 최대공약수를 구할 수 있다.
>
> 두 수의 최소공배수는 두 수의 곱 / gcd(n,m)을 이용하면 쉽게 계산 가능하다.

<br>

소스코드는 다음과 같다.

```python
from math import gcd

def solution(n, m):
    return [gcd(n,m), n*m // gcd(n,m)]
```



<br>

<br>

[최대공약수와 최소공배수 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/최대공약수와%20최소공배수.py)

<br>
