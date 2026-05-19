[Question](https://leetcode.com/problems/odd-even-linked-list/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def oddEvenList(self, head):
        if not head or not head.next:
            return head
        odd = head
        even = head.next
        evenHead = even
        while even and even.next:
            odd.next = even.next
            odd = odd.next
            even.next = odd.next
            even = even.next
        odd.next = evenHead
        return head 
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2516" height="949" alt="image" src="https://github.com/user-attachments/assets/ef13dbe0-86d6-4045-820b-cb5ec1477288" />
