[Question](https://leetcode.com/problems/balanced-binary-tree/description/)


## Implementation
```python
def isBalanced(self, root):
        def dfs(root):
            if not root:
                return 0
            left = dfs(root.left)
            if left == -1:
                return -1
            right = dfs(root.right)
            if right == -1:
                return -1
            if abs(left - right) > 1:
                return -1
            return 1 + max(left, right)
        return dfs(root) != -1
```
  ## Complexities
- Time complexity: O(n)
- Space complexity: O(h)
<img width="2559" height="1108" alt="image" src="https://github.com/user-attachments/assets/7a9d89a0-7043-420a-95fe-7adec23ba8f4" />
