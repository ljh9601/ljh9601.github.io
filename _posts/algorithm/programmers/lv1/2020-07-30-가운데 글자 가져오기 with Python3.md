---
layout: post
title: (LV1) 가운데 글자 가져오기 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

## LV1. 연습문제 - 가운데 글자 가져오기


![](/Users/Janghaeng/Desktop/ljh9601.github.io/assets/img/가운데 글자 가져오기.png)

<br><br>

```
1. s의 길이를 구한다.

2. s의 길이가 짝수, 홀수일 때로 나눈다.
	2-1. 짝수일 경우 length // 2 - 1과 length // 2 를 더한다.
	2-2. 홀수일 경우 length // 2 를 더한다.

3. 더한 스트링을 반환한다.
```

<br>

코드를 첨부하고 포스팅을 마치도록 하겠다.

```python
def solution(s):
    length = len(s)
    ans = ""
    if length % 2 == 0 :
        ans += s[length // 2 - 1] + s[length // 2]
    else :
        ans = s[length // 2]
    return ans
```

<br>

[가운데 글자 가져오기 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/가운데%20글자%20가져오기.py)



