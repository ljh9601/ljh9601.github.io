---
layout: post
title: (LV1) 문자열 내림차순으로 배치하기 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

## Lv1. 연습문제 - 문자열 내림차순으로 배치하기

<br>


![](/assets/img/문자열%20내림차순으로%20배치하기.png)

<br>

> 
>
> 1. Unicode에서 대문자가 소문자보다 앞에 있다.
>
> 2. 1번을 이용해 내림차순 정렬 후 string으로 바꾸면 끝!

<br>

소스코드는 다음과 같다.

```python
def solution(s):
    return ''.join(sorted(s, reverse=True))
```



<br>

<br>

[문자열 내림차순으로 배치하기 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/문자열%20내림차순으로%20배치하기.py)