[Question](https://leetcode.com/problems/diameter-of-binary-tree/description/)


## Implementation
```python
def diameterOfBinaryTree(self, root: Optional[TreeNode]) -> int:
        res = 0

        def dfs(root):
            nonlocal res
            if not root:
                return 0
            
            l = dfs(root.left)
            r = dfs(root.right)

            
            res = max(res, l + r)
            
            return 1 + max(l, r)

        dfs(root)
        return res
```
  ## Complexities
- Time complexity: O(n)
- Space complexity: O(h)
<img width="2549" height="1027" alt="image" src="https://github.com/user-attachments/assets/d3613e95-c7e9-4de8-89b4-3d80c83df8c5" />
