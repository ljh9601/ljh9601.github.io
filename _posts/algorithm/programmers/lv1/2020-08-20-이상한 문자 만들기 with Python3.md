---
layout: post
title: (LV1) 이상한 문자 만들기 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

## Lv1. 연습문제 - 이상한 문자 만들기

<br>



![](https://i.imgur.com/ooqfMmh.png)

<br>

> 1. 문자열을 탐색하며
>
>    
>
> 2. 알파벳일 경우
>
>    > 짝수 인덱스라면 대문자(upper())
>    >
>    > 홀수 인덱스라면 소문자(lower())
>
>    후 인덱스를 1 더해준다.
>
>    
>
> 3. 공백일 경우 그냥 더해주고 인덱스를 초기화한다. (**단어 인덱스 초기화**)
>
>    
>
> 4. 그 이외의 문자일 경우 역시 그냥 더해준다.

<br>

소스코드는 다음과 같다.

```python
def solution(s):
    answer = ""
    idx = 0
    for i in range(len(s)):
        if s[i] == ' ':
            answer += s[i]
            idx = 0
            continue
        if s[i].isalpha():
            if not idx % 2:
                answer += s[i].upper()
            else :
                answer += s[i].lower()
        else :
            answer += s[i]
        idx += 1
    return answer
```



<br>

<br>

[이상한 문자 만들기 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/이상한%20문자%20만들기.py)

<br>