[Question](https://leetcode.com/problems/merge-two-sorted-lists/description/)


## Implementation
Optimal solution
```python
class ListNode(object):
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next
class Solution(object):
    def mergeTwoLists(self, list1, list2):
        dummy = ListNode(0)
        current = dummy
        while list1 and list2:
            if list1.val >= list2.val:
                current.next = list2
                list2 = list2.next
            else:
                current.next = list1
                list1 = list1.next
            current = current.next
        current.next = list1 or list2
        return dummy.next 
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2529" height="1009" alt="image" src="https://github.com/user-attachments/assets/63815aeb-603e-40b3-b4eb-f0cc814ad8d0" />

