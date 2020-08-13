---
layout: post
title: (LV1) 문자열 다루기 기본 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

## Lv1. 연습문제 - 문자열 다루기 기본

<br>



![](/assets/img/문자열%20다루기%20기본.png)

<br>

> 
>
> 1. len(s)가 4 혹은 6이고, 
>
> 2. s가 정수범위인지 확인하는 isdecimal() 혹은 isdigit() 함수를 사용한다.

<br>

소스코드는 다음과 같다.

```python
def solution(s):
    return len(s) in [4, 6] and s.isdecimal()
```



<br>

<br>

[문자열 다루기 기본 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/문자열%20다루기%20기본.py)

<br>