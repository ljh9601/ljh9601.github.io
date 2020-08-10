---
layout: post
title: (LV1) 문자열 내 마음대로 정렬하기 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

## Lv1. 연습문제 - 문자열 내 마음대로 정렬하기

<br><br>

![](/assets/img/문자열%20내%20마음대로%20정렬하기.png)

<br>

쉬운 문제다. 바로 로직을 설명해보겠다.

<br>

> 
>
> <b>1. 먼저 strings 배열을 정렬한다</b>
>
>    > 여기서 정렬하는 이유는 2번을 실행하기 전 **사전순으로 먼저 정렬**하기 위함.
>    > 이래야만 n번째 인덱스 기준 정렬을 해도 사전순으로 잘 정렬됨.
>
> <b>2. 문자열의 해당 인덱스를 기준으로 정렬한다.</b>

<br>

소스코드는 다음과 같다.

```python
def solution(strings, n):
    return sorted(sorted(strings), key = lambda x : x[n])
```
<br>

<center><b>lambda 식을 이용해 각 스트링의 n번째 값을 정렬 기준으로 설정해주었다.</b></center>

<br>

<br>

[문자열 내 마음대로 정렬하기 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/문자열%20내%20마음대로%20정렬하기.py)

