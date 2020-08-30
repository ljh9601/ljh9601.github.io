---
layout: post
title: (LV1) 키패드 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1, 2020카카오인턴십]
comments: true
---

## Lv1. 2020 카카오 인턴십 - 키패드 누르기

<br>
<br>

![](https://i.imgur.com/xIrY7oj.png)

![](https://i.imgur.com/wvFLRUW.png)

<br>

> 휴대폰 키패드를 하나의 배열로 생각해보자.
>
> 1의 위치는 (0,0), 2는 (0,1), 3은 (0,2), 4는 (1,0) ... #은 (3,2)가 된다.
>
> 여기서 *을 10, 0을 11, #을 12로 차례대로 증가하는 수로 생각하면 일반화가 된다.
>
> 즉 숫자를 알면 (x,y) = ( (number - 1) // 3, (number + 2) % 3 ) 이다!
>
> 1. 왼손의 초기 위치는 (3,0), 오른손의 초기 위치는 (3,2)로 설정해준다.
>
> 2. numbers를 순회하며
>
>    2-1. [1, 4, 7]이면 무조건 왼손, [3, 6, 9]라면 무조건 오른손은 보장되어있다.
>
> 3. [2, 5, 8]일 경우 맨해튼 거리를 사용해 거리의 대소비교를 해주고, 더 가까운 손을 이동시킨다. 
>
>    3-1. 유클리드 거리를 사용해도 되지만, 맨해튼 거리가 계산식이 훨씬 간단하기 때문에 맨해튼 거리를 사용했다.
>
>    3-2. 거리가 같다면 오른손잡이, 왼손잡이인지 보고 주손을 이동시키면 된다.
>
> 4. answer에 이용한 손을 append해준다!

<br>

소스코드는 다음과 같다.

```python
def solution(numbers, hand):
    answer = ''
    # 왼손, 오른손의 초기 좌표 설정
    leftPos = (3,0); rightPos = (3,2)
    for val in numbers :
        # 0인 경우 좌표처리를 위해 따로 예외처리
        if val == 0:
            val = 11
        # 눌러야 할 숫자의 좌표를 valPos에 저장
        valPos = ((val-1)//3, (val+2)%3)
        
        # 눌러야 할 숫자가 1,4,7 중에 하나라면 무조건 왼손
        if val in [1,4,7]:
            answer += 'L'
            leftPos = valPos
            continue
            
        # 눌러야 할 숫자가 3,6,9 중에 하나라면 무조건 오른손
        elif val in [3,6,9]:
            answer += 'R'
            rightPos = valPos
            continue
            
        # 거리의 대소 비교만 하면 되기 때문에 맨해튼 거리를 사용
        distLeft = abs(valPos[0] - leftPos[0]) + abs(valPos[1] - leftPos[1])
        distRight = abs(valPos[0] - rightPos[0]) + abs(valPos[1] - rightPos[1])
        
        # 왼손과 오른손 사이의 값이 같다면 오른손잡이라면 오른손, 왼손잡이라면 왼손 이동
        if distLeft == distRight :
            if hand == 'left':
                answer += 'L'
                leftPos = valPos
            else :
                answer += 'R'
                rightPos = valPos
        else :
            if distLeft < distRight :
                answer += 'L'
                leftPos = valPos
            else :
                answer += 'R'
                rightPos = valPos
    return answer
```



<br>

<br>

[키패드 누르기 Github에서 보기](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/키패드%20누르기.py)