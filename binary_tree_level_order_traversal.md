[Question](https://leetcode.com/problems/binary-tree-level-order-traversal/description/)


## Implementation
Optimal solution
```python
from collections import deque
class Solution(object):
    def levelOrder(self, root):
        if not root:
            return []
        ans = []
        def dfs(root, level):
            if not root:
                return 
            if len(ans) == level:
                ans.append([])
            ans[level].append(root.val)
            dfs(root.left, level + 1)
            dfs(root.right, level + 1)
        dfs(root, 0)
        return ans
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(h)
<img width="1440" height="770" alt="image" src="https://github.com/user-attachments/assets/117a9538-c80e-4252-ad3a-c057a5bd4e84" />
