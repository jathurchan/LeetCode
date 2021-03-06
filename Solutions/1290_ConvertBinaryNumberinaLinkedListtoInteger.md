# 1290. Convert Binary Number in a Linked List to Integer

## Description

Given `head` which is a reference node to a singly-linked list. The value of each node in the linked list is either 0 or 1. The linked list holds the binary representation of a number.

Return the *decimal value* of the number in the linked list.

**Example 1:**

![graph-1.png](https://assets.leetcode.com/uploads/2019/12/05/graph-1.png)

**Input:** head = [1,0,1]

**Output:** 5

**Explanation:** (101) in base 2 = (5) in base 10

**Example 2:**

**Input:** head = [0]

**Output:** 0

**Example 3:**

**Input:** head = [1]

**Output:** 1

**Example 4:**

**Input:** head = [1,0,0,1,0,0,1,1,1,0,0,0,0,0,0]

**Output:** 18880

**Example 5:**

**Input:** head = [0,0]

**Output:** 0

**Constraints:**

- The Linked List is not empty.
- Number of nodes will not exceed `30`.
- Each node's value is either `0` or `1`.

## Solution

Runtime: 46 ms, faster than 5.51% of Python online submissions for Convert Binary Number in a Linked List to Integer.

Memory Usage: 13.7 MB, less than 14.05% of Python online submissions forConvert Binary Number in a Linked List to Integer.

```python
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution(object):
    def getDecimalValue(self, head):    
        """
        :type head: ListNode
        :rtype: int
        """
        
        result = 0
        
        # ----  1st Solution

        # while head:
        #     result = 2 * result + head.val
        #     head = head.next

        # ---- 2nd Solution

        while head:
            result = (result<<1) + head.val
            head = head.next
        
        return result
```