---
layout: post
title: (LV1) 시저 암호 with Python3
category: 프로그래머스
tags: [알고리즘, 프로그래머스, Lv1]
comments: true
---

## Lv1. 연습문제 - 시저 암호

<br>



![](https://i.imgur.com/pL5ZMF8.png)

<br>

> 이 문제는 ord, chr 함수만 알고 있으면 된다.
>
> > **ord : 문자를 아스키코드로 변환해준다.**
> >
> > **chr : 아스키코드를 문자로 변환해준다.**
>
> 1. **대문자와 소문자 배열**을 만들어둔다.
> 2. s를 순회하며 **ord() 함수로 각 문자의 아스키코드**를 구한다.
> 3. **아스키코드 + n**을 한 후 이를 다시 **chr() 함수로 문자로 변환**한다.
> 4. 알파벳이 넘어가면 다시 처음으로 돌아오므로 **% 26**으로 계산해준다.

<br>

소스코드는 다음과 같다.

```python
def solution(s, n):
    ans = ''
    small = [chr(ord('a') + i) for i in range(26)]
    big = [chr(ord('A') + i) for i in range(26)]
    for ch in s:
        if ch.isalpha():
            ans += small[(small.index(ch)+n)%26] if ch.islower() else big[(big.index(ch)+n)%26]
        else :
            ans += ch
    return ans
```



<br>

<br>

[시저 암호 Github에서 보기]([https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/%EC%8B%9C%EC%A0%80%20%EC%95%94%ED%98%B8.Py](https://github.com/ljh9601/BOJ-Programmers/blob/master/Programmers/Lv1/시저%20암호.Py))

<br>