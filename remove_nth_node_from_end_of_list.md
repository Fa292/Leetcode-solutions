[Question](https://leetcode.com/problems/remove-nth-node-from-end-of-list/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def removeNthFromEnd(self, head, n):
        fast = head
        slow = head
        for i in range(n):
            fast = fast.next
        if fast is None:
            head = head.next
            return head    
        while fast.next:
            slow = slow.next
            fast = fast.next
        
        
        slow.next = slow.next.next
        return head
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2547" height="975" alt="image" src="https://github.com/user-attachments/assets/09391788-2ff2-4079-a491-541d3d77a28e" />
