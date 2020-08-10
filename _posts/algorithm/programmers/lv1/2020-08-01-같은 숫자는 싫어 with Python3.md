---
layout: post
title: (LV1) 같은 숫자는 싫어 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

## Lv1. 연습문제 - 같은 숫자는 싫어

<br>

![](/assets/img/같은%20숫자는%20싫어.png)

<br>
나온 숫자들을 차례대로 배열에 집어넣으면 되는 문제다.

Set, dictionary 등으로 풀려고 했지만, 중복된 원소가 뒤에 다시 나올 수 있다는 조건이 있어 배열로 편하게 brute force로 진행했다.

<br>

문제 조건이 0~9 사이의 수이므로 초기 array에 나올 수 없는 수인 -1을 넣고, 

배열을 순회하며 answer의 마지막 원소와 값이 다른 경우에 answer에 append해준다.

소스코드는 다음과 같다.

```python
def solution(arr):
    answer = [-1]
    for i in arr :
        if i != answer[-1] :
            answer.append(i)
    answer.pop(0)
    return answer
```

<br>

[같은 숫자는 싫어 소스 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/같은%20숫자는%20싫어.py)

