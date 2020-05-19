---
layout:     post
title:      "Leet Code Day 2"
date:       2020-5-19
author:     "Qiansu"
tags:
    - Leetcode
---

## Reverse integer

Given a 32-bit signed integer, reverse digits of an integer.

Java solution

```Java

class solution{
  public int reverseInt(int x ){
    int  r = 0;
    while(x != 0){
      int a = x % 10;
      x  = x /10 ;
      if(r > Integer.MAX_VALUE /10 || r < Integer.MIN_VALUE /10 ){
                 return 0;
             }
             r = r * 10 + a;

         }
         return r;
    }
  }
```

Python soluton

```python

class solution

def reverse (self, x: int) -> int

if x > 0 :
  a = int(str(x) [:: -1])
if x < 0:
  a =  - 1 * int(str(x * -1)[:: -1])

min = -2 *32
max = 2*32 -1

if  a not in range(min, max):
  return 0

else:
  return a

```
## palindrome Numebr

Ex 121

Determine whether an integer is a palindrome. An integer is a palindrome when it reads the same backward as forward.



Python solution
```python

class solution:
def isPalindrome(self, x :int) -> bool:
  return (str(x) == str(x)[:: -1])
```

Java solution

```java

class solution {
public boolean isPalindorm (int x){
  while(x < 0 || (x % 10 && x!= 0) ){

    return  false;
  }
  int r = 0;
  while (x > r){
    r = r * 10 + x %10;
    x = x /10;



  }
  return x == r || x == r/10;



}
}



```
