[Question](https://leetcode.com/problems/rotate-list/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def rotateRight(self, head, k):
        if not head or not head.next or k == 0:
            return head
        tail = head
        length = 1
        while tail.next:
            length += 1
            tail = tail.next
        k %= length
        if k == 0:
            return head
        pos = length - k - 1
        tail.next = head
        newTail = head
        for i in range(pos):
            newTail = newTail.next
        newHead = newTail.next
        newTail.next = None
        return newHead
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2504" height="931" alt="image" src="https://github.com/user-attachments/assets/e7953552-8bb0-4d4b-8256-d6f26b919698" />
