---
layout: post
title: (LV1) 하샤드 수 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

<br>

## Lv1. 연습문제 - 하샤드 수

<br>



![](https://i.imgur.com/QKUMVTl.png)

<br>

> 1. x를 string으로 바꾼다.
>
>    
>
> 2. Str(x)를 순회하며 한자리씩 int로 다시 바꿔준 후 sum()을 구한다.
>
>    
>
> 3. % 연산자를 이용해 x와 나누어지는지 여부를 확인한다.

<br>

소스코드는 다음과 같다.

```python
def solution(x):
    return not x % sum([int(v) for v in str(x)])
```



<br>

<br>

[하샤드 수 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/하샤드%20수.py)

<br>