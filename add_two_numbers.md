[Question](https://leetcode.com/problems/add-two-numbers/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def addTwoNumbers(self, l1, l2):
        dummy = ListNode(0)
        output = dummy
        rem = 0
        while l1 or l2:
            val1 = l1.val if l1 else 0
            val2 = l2.val if l2 else 0
            add = int(val1) + int(val2) + rem
            
            digit = add % 10
            rem = add // 10 
            
            output.next = ListNode(digit)
            output = output.next
            if l1:
                l1 = l1.next
                
            if l2:
                l2 = l2.next
        if rem:
            output.next = ListNode(rem)
            
        return dummy.next 
```
## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2544" height="1022" alt="image" src="https://github.com/user-attachments/assets/34c582da-0738-495d-b683-703af7e919aa" />
