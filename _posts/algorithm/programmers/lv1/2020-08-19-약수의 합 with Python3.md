---
layout: post
title: (LV1) 약수의 합 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

## Lv1. 연습문제 - 약수의 합

<br>


ㅠㅜㅗㅛㅓㅡ뎌
![](https://i.imgur.com/cTgzfTM.png)

<br>

> 이 문제는 최적화를 까먹기 쉬운 문제다. 
>
> **route(n)**까지만 검사해주면 되는데도 말이다!
>
> 1. n이 0과 1일 때는 예외처리해준다.
>
>    
>
> 2. **1부터 route(n)**까지 loop를 돌며 약수를 구한다.
>
>    
>
> 3. 만약 약수라면 제곱수일 때를 생각해줘야 한다.
>
>    > 4의 약수는 1, 2, 4인데 **2 * 2는 4**이므로 이럴 땐 한번만 더해준다.
>
>    
>
> 4. answer 반환!

<br>

소스코드는 다음과 같다.

```python
import math

def solution(n):
    if n < 2 :
        return n
    answer = 0
    for i in range(1, int(math.sqrt(n)) + 1):
        if not n % i:
            answer += (i + (n // i)) if i != (n // i) else i
    return answer
```



<br>

<br>

[약수의 합 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/약수의%20합.py)

<br>