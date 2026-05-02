[Question](https://leetcode.com/problems/intersection-of-two-linked-lists/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def getIntersectionNode(self, headA, headB):
        if not headA or not headB:
            return None
        a = headA
        b = headB
        while a != b:
            a = a.next if a else headB
            b = b.next if b else headA
        return a
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2545" height="963" alt="image" src="https://github.com/user-attachments/assets/e317fad8-5e02-4009-b22f-1c0f1e198886" />
