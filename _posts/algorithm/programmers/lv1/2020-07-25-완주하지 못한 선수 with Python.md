---
layout: post
title: (LV1)완주하지 못한 선수 with Python3
tags: [알고리즘, 프로그래머스]
category: [algorithm, programmers]
comments: true
---
# Lv1. 해시 - 완주하지 못한 선수

![](/Users/Janghaeng/Downloads/beautiful-jekyll-master/assets/img/완주하지 못한 선수.png)

이 문제의 프로그래머스 공식 알고리즘 분류는 "해시"이다. 하지만 해시로 풀 필요가 전혀 없는 문제이다. 그 근거는

​	**participant 배열과 completion 배열에서 다른 원소는 단 하나이다.**

라는 것인데, Python3의 zip 을 활용하면 손쉽게 풀 수 있는 문제다. zip은 Python의 내장함수로, 두 리스트를 하나의 연관된 리스트로 묶어준다.

**묶는 순서는 리스트의 맨 앞에서부터 차례대로**라는 것을 명심하길 바란다.

따라서 participant와 completion을 알파벳 오름차순, 혹은 내림차순으로 정렬한 다음, 두 리스트를 zip으로 묶어 비교하며 만약 두 원소가 다를 경우 return해주면 된다! 물론 return은 participant의 값으로 해줘야 한다. 

쉬운 문제고, 두 배열을 단지 비교할 수도 있지만, 파이썬 유저라면 zip 함수 써볼 수 있는 좋은 기회라고 생각한다.

소스코드는 다음과 같다.

```python
def solution(participant, completion):
    participant.sort()
    completion.sort()
    for part, comp in zip(participant, completion):
        if part != comp :
            return part
    return participant[-1]
```

[완주하지 못한 선수 소스 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/완주하지%20못한%20선수.py)