[Question](https://leetcode.com/problems/swap-nodes-in-pairs/description/)


## Implementation
Optimal solution
```python
def swapPairs(self, head):
        if not head or not head.next:
            return head
        dummy = ListNode(0)
        dummy.next = head
        prev = dummy
        while prev.next and prev.next.next:
            left = prev.next
            right = left.next
            left.next = right.next
            right.next = left
            prev.next = right
            prev = left
        return dummy.next
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2526" height="929" alt="image" src="https://github.com/user-attachments/assets/7a33a33f-4c57-4472-a7fd-9482e0c5e5f6" />
