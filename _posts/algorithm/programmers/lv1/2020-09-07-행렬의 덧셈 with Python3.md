---
layout: post
title: (LV1) 행렬의 덧셈 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

<br>

## Lv1. 연습문제 - 행렬의 덧셈

<br>



![](https://i.imgur.com/XAMjF9j.png)

<br>

> 1. 두 행렬의 (i,j)를 순회하며 더한 값을 return 배열에 저장한다....

<br>

소스코드는 다음과 같다.

```python
def solution(arr1, arr2):
    return [[a+b for a, b in zip(arr1[i], arr2[i])] for i in range(len(arr1))]
```



<br>

<br>

[행렬의 덧셈 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/행렬의%20덧셈.py)

<br>