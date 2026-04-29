[Question](https://leetcode.com/problems/linked-list-cycle/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def hasCycle(self, head):
        slow = head
        fast = head
        while fast and fast.next:
            slow = slow.next
            fast = fast.next.next
            if slow == fast:
                return True
        return False
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2535" height="1018" alt="image" src="https://github.com/user-attachments/assets/25cbee73-1647-4e19-b82b-e4d04e301a53" />
