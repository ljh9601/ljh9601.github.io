---
layout: post
title: (LV1) 모의고사 with Python3
tags: [알고리즘, 프로그래머스]
category: [programmers, Level1]
comments: true
---
## LV1. 완전탐색 - 모의고사



![](/Users/Janghaeng/Desktop/ljh9601.github.io/assets/img/모의고사.png)

이 문제를 풀고 난 후 가장 후회했던 점은 굳이 편하게 짤 수 있는 로직을 고민했다는 점이다. 풀고보니 간단명료하게 static한 배열로 푸는 것이 훨씬 편하다고 생각했다.<br><br>

1. 수포자가 3명으로 고정이라는 점
2. 3명의 패턴이 항상 일정하다는 점

<br> 이 바로 그 이유인데, 나는 바보처럼 굳이 3명의 반복 로직을 코드로 구현하려 했다.  

<br> Person1 = [1, 2, 3, 4, 5]

Person2 = [2, 1, 2, 3, 2, 4, 2, 5]

Person3 = [3, 3, 1, 1, 2, 2, 4, 4, 5, 5]

<br> 로 구성하고, 반복문을 돌려 정답의 개수만 찾았으면 됐을 텐데!

후에 코드를 다시 보니 자신이 한심하다.

어렵지 않은 문제니 코드를 첨부하고 포스팅을 마치도록 하겠다.

```python
'''
모의고사
'''

#1번 : 1 2 3 4 5 반복
#2번 : (2,1) (2,3), (2,4), (2,5) 반복 
#3번 : 3,1,2,4,5 순서대로 각각 2번씩 반복

def solution(answers):
    answer = []
    answer.append([0, 1])
    answer.append([0, 2])
    answer.append([0, 3])
    personTwo = [2, 1, 2, 3, 2, 4, 2, 5]
    personThree = [3, 3, 1, 1, 2, 2, 4, 4, 5, 5]
    for i in range(len(answers)):
        if (i % 5) + 1 == answers[i] :
            answer[0][0] += 1
        if answers[i] == personTwo[i%8] :
            answer[1][0] += 1
        if answers[i] == personThree[i%10] :
            answer[2][0] += 1
    maxPerson = max(answer[0][0], answer[1][0], answer[2][0])
    result = []
    for i in range (0, len(answer)) :
        if maxPerson == answer[i][0] :
            result.append(answer[i][1])
    return sorted(result)
```

[모의고사 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/모의고사.py)

