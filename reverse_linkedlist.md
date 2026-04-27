[Question](https://leetcode.com/problems/reverse-linked-list/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def reverseList(self, head):
        curr = head
        prev = None
        while curr:
            next_node = curr.next
            curr.next = prev
            prev = curr
            curr = next_node
        return prev
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)

<img width="2524" height="948" alt="image" src="https://github.com/user-attachments/assets/ccdbb0d8-5fcd-4947-9fc3-7c586709a0ee" />
