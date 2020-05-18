---
layout: post
title: "Leetcode Day1"
subtitle: ''
author: "Qiansu"
header-style: text
header-image: "img/post-bg-halting.jpg"
tags:
  - Leetcode
---

## Two Sum


<p>Given an array of integers, return indices of the two numbers such that they add up to a specific target.
You may assume that each input would have exactly one solution, and you may not use the same element twice.</p><br>

java solution

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        for (int i = 0; i < nums.length;i++){
            for (int j = i+1; j<nums.length; j++){
                if (nums[j] == target -nums[i]){
                    return new int[]{i,j
                    };
                }
            }
        }
        throw new IllegalArgumentException("No two sum solution");
    }}
```
Python solution

```python
class Solution(object):
  def twoSum(self,nums,target):
    r = {}
    for i in range(len(nums)):
      if target -nums[i] in r:
        return [r[target - nums[i]],i]
      else:
        r[nums[i]] = i
```

## Add Two Number ListNode

You are given two non-empty linked lists representing two non-negative integers. The digits are stored in reverse order and each of their nodes contain a single digit. Add the two numbers and return it as a linked list.


Java solution


 ```java
public ListNode AddTwoNumbers(ListNode l1,ListNode l2){
  ListNode Head = new ListNode(0);
  ListNode p = l1, q = 12, curr = Head;

  while (p != null || q != null){

       ListNode dummyHead = new ListNode(0);
       ListNode p = l1, q = l2, curr = dummyHead;
       int carry = 0;
       while (p != null || q != null) {
           int x = (p != null) ? p.val : 0;
           int y = (q != null) ? q.val : 0;
           int sum = carry + x + y;
           carry = sum / 10;
           curr.next = new ListNode(sum % 10);
           curr = curr.next;
           if (p != null) p = p.next;
           if (q != null) q = q.next;
       }
       if (carry > 0) {
           curr.next = new ListNode(carry);
       }
       return dummyHead.next;


  }

}
```
