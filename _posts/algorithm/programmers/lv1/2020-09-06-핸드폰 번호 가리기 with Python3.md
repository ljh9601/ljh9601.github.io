---
layout: post
title: (LV1) 핸드폰 번호 가리기 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

<br>

## Lv1. 연습문제 - 핸드폰 번호 가리기

<br>



![](https://i.imgur.com/RcVlwVa.png)

<br>

> 1. String slicing을 통해 마지막 4자리 전까지의 길이만큼 "*"을 만든다.
>
>    
>
> 2. 마지막 4자리를 1번에서 만든 스트링 뒤에 더한다.

<br>

소스코드는 다음과 같다.

```python
def solution(phone_number):
    return '*' * (len(phone_number[:-4])) + phone_number[-4:]
```



<br>

<br>

[핸드폰 번호 가리기 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/핸드폰%20번호%20가리기.py)

<br>