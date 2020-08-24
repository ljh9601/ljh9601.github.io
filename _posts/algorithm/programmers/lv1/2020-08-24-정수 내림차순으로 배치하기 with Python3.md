---
layout: post
title: (LV1) 정수 내림차순으로 배치하기 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---



## Lv1. 연습문제 - 정수 내림차순으로 배치하기

<br>


![](https://i.imgur.com/5GiXMNV.png)

<br>

> 1. n을 string으로 바꾼 후 내림차순으로 정렬한다.
>
> 2. Join()을 이용해 string으로 바꾼 후 int형으로 형변환해주면 끝!

<br>

소스코드는 다음과 같다.

```python
def solution(n):
    return int(''.join(sorted(str(n), reverse=True)))
```



<br>

<br>

[정수 내림차순으로 배치하기 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/정수%20내림차순으로%20배치하기.py)