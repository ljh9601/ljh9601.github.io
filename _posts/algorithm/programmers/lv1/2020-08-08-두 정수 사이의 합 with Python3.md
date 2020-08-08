---
layout: post
title: (LV1) 두 정수 사이의 합 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

## Lv1. 연습문제 - 두 정수 사이의 합

<br>



![](/assets/img/두%20정수%20사이의%20합.png)

<br>

이 문제 역시 Short 코딩을 좋아하는 사람의 입장에서 되게 좋았다! 로직은 무척 간단하다.

> <center><b>그냥 다 더하자.. 작은 수부터 큰 수까지<b></center>

<br>

소스코드는 다음과 같다.

```python
def solution(a, b):
    return sum([val for val in range(min(a,b),max(a,b)+1)])
```

<br>

코드를 풀어보면

```python
1. a, b 중 작은 수와 큰 수를 정해준다.
2. min(a,b), max(a,b)까지 정수 배열을 만든다.
3. 배열의 sum을 구해준다.
```



<br>

<br>

[두 정수 사이의 합 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/두%20정수%20사이의%20합.py)

