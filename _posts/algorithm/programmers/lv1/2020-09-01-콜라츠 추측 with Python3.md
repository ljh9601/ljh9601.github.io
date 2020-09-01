---
layout: post
title: (LV1) 콜라츠 추측 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

<br>

## Lv1. 연습문제 - 콜라츠 추측

<br>


![](https://i.imgur.com/VjQ69sJ.png)

<br>

> num이 1보다 클 동안 짝수라면 2로 나누고, 홀수라면 3을 곱하고 1을 더해주며
>
> 연산 횟수가 500이 넘으면 -1을 return하면 된다!

<br>

소스코드는 다음과 같다.

```python
def solution(num):
    cnt = 0
    while num > 1 :
        if cnt > 500:
            return -1
        num = num // 2 if not num % 2 else num * 3 + 1
        cnt += 1
    return cnt
```



<br>

<br>

[콜라츠 추측 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/콜라츠%20추측.py)

<br>