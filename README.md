# Geeks for Geeks: [30 Days of Code](https://practice.geeksforgeeks.org/courses/30-days-of-code)

## Overview

Committing to a new habit can be tough, especially when you are just starting out. We’ve got for you the ‘30 days of Code’ challenge wherein you will be given a new coding problem every day at 12:00 AM IST and you have only 24 hours to submit your answers. The 30-day-challenge comprises of 21 different DSA topics and the cumulative scores of all the days shall determine your score.

Brownie points: After submitting your answer, take the screenshot of the submission and upload it on your Twitter handle and tag us @geeksforgeeks with the #30daysofcodewithGFG.We have a surprise for you ;)

More correct answers you get, more chances of you being on the top of the leaderboard! Don’t miss out on the 1st challenge which will be uploaded on 26th January, 12:01 AM IST.

_N.B. I missed the first 3 days, due to not knowing about the competition. Started keeping track of my code and questions on Day 7 when I realized they each dissapear after 48 hours_

## Day 7 - Valid Pair Sum

Given an array of size N, find the number of distinct pairs {a[i], a[j]} (i != j) in the array with their sum greater than 0.

Example 1:

Input: N = 3, a[] = {3, -2, 1}
Output: 2
Explanation: {3, -2}, {3, 1} are two 
possible pairs.

Example 2:

Input: N = 4, a[] = {-1, -1, -1, 0}
Output: 0
Explanation: There are no possible pairs.

Your Task:  
You don't need to read input or print anything. Complete the function ValidPair() which takes the array a[ ] and size of array N as input parameters and returns the count of such pairs.

Expected Time Complexity: O(N * Log(N))
Expected Auxiliary Space: O(1)

Constraints:
1 ≤ N ≤ 105 
-104  ≤ a[i] ≤ 104


## Day 7: Code
```python
class Solution:
    def ValidPair(self, a, n): 
    	p = 0 
    	q = len(a) - 1
    	s = 0
    	a.sort()
    	while p<q:
	        if (a[p]+a[q]>0):
    	        s += q-p
    	        q -= 1
    	    else:
    	        p += 1
        return s
  ```
