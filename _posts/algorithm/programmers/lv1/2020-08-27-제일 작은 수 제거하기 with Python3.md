---
layout: post
title: (LV1) 제일 작은 수 제거하기 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

## Lv1. 연습문제 - 제일 작은 수 제거하기

<br>
<br>


![](https://i.imgur.com/altozsp.png)

<br>

> 1. min 함수를 이용해 최솟값을 구하고, arr에서 remove로 제거한다.
>
>    
>
> 2. arr에 원소가 하나 이상 있다면 arr, 없다면 [-1] return

<br>

소스코드는 다음과 같다.

```python
def solution(arr):
    arr.remove(min(arr))
    return arr if arr else [-1]
```



<br>

<br>

[제일 작은 수 제거하기 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/제일%20작은%20수%20제거하기.py)