---
layout: post
title: (LV1) 자연수 뒤집어 배열로 만들기 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---



## Lv1. 연습문제 - 자연수 뒤집어 배열로 만들기

<br>



![](https://i.imgur.com/hU5vePe.png)

<br>

> 1. 정수를 String으로 바꿔준 후 뒤집는다! ([::-1])
>
>    
>
> 2. return 배열에 각 값을 int형으로 바꾸어 넣는다.

<br>

소스코드는 다음과 같다.

```python
def solution(n):
    return [int(v) for v in str(n)[::-1]]
```



<br>

<br>

[자연수 뒤집어 배열로 만들기 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/자연수%20뒤집어%20배열로%20만들기.py)

<br>