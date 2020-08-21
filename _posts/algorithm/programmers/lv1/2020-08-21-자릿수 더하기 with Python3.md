---
layout: post
title: (LV1) 자릿수 더하기 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---



## Lv1. 연습문제 - 자릿수 더하기

<br>



![](https://i.imgur.com/d2dnags.png)

<br>

> 1. 정수를 String으로 바꿔준 후
>
>    
>
> 2. 각 숫자를 순회하며 int로 다시 바꾸어 answer에 더해준다!

<br>

소스코드는 다음과 같다.

```python
def solution(n):
    return sum([int(v) for v in str(n)])
```



<br>

<br>

[자릿수 더하기 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/자릿수%20더하기.py)

<br>