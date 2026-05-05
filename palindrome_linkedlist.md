[Question](https://leetcode.com/problems/palindrome-linked-list/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def isPalindrome(self, head):
        left = head
        right = head
        
        while right and right.next:
            left = left.next
            right = right.next.next
        middle = left.next if right else left
        
        prev = None
        while middle:
            next_node = middle.next
            middle.next = prev
            prev = middle
            middle = next_node
        left = head
        while left and prev:
            if left.val != prev.val:
                return False
            left = left.next
            prev = prev.next
        return True 
```
## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2519" height="1013" alt="image" src="https://github.com/user-attachments/assets/79bdda7a-fc89-40e7-ad49-c463ea2c049b" />


