---
layout: post
title: (LV1) 체육복 with Python3
category: [algorithm, programmers, lv1]
tags: [알고리즘, 프로그래머스]
comments: true
---

# LV1. 탐욕법 - 체육복



![](/Users/Janghaeng/Desktop/ljh9601.github.io/assets/img/체육복.png)

이 문제는 알고리즘 분류에 나와있듯이 Greedy하게, 즉 체육복을 잃어버린 사람에게 빌려주면서 풀면 되는 문제다.<br>

또한 여분이 있는 사람이 체육복을 잃어버릴 경우 체육 수업에는 참여할 수 있지만 빌려주지는 못하는 사람이 되므로, lost와 reverse 배열 모두에 존재하는 사람은 이 문제에 관여할 수 있는 여지가 없다. <br><br>따라서 lost 배열과 reverse 배열을 set 형태로 만들고, 각각의 차집합을 구했다. <br>

마지막으로 반복문을 돌며 reserve 배열이 현재 참조하는 값 - 1 이 lost 배열에 있다면 lost에서 빼주고, 없다면 + 1을 검사하여 pop해준다. <br>

여기서 순서가 굉장히 중요한데, n+1번 사람이 n번을 먼저 빌려줘야 한다! <br>n번 사람이 n+1번 사람을 먼저 확인하는 경우 예외가 발생하게 된다. 

```python
def solution(n, lost, reserve):
    reserve_set = set(reserve) - set(lost)
    lost_set = set(lost) - set(reserve)
    for current in reserve_set:
        if current - 1 in lost_set :
            lost_set.remove(current-1)
        elif current + 1 in lost_set :
            lost_set.remove(current+1)
            
    return n - len(lost_set)
```

[체육복 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/체육복.py)

