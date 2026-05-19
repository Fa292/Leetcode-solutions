[Question](https://leetcode.com/problems/delete-node-in-a-linked-list/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def deleteNode(self, node):
        node.val = node.next.val
        node.next = node.next.next
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2525" height="954" alt="image" src="https://github.com/user-attachments/assets/e2f1df9f-9003-4720-803e-c2fc8e91f8bf" />
