[Question](https://leetcode.com/problems/validate-binary-search-tree/description/)


## Implementation
Optimal solution
```python
def isValidBST(self, root: TreeNode | None) -> bool:
        def dfs(root, lower, upper):
            if not root:
                return True
            if root.val <= lower or root.val >= upper:
                return False
            left = dfs(root.left, lower, root.val)
            right = dfs(root.right, root.val, upper)
            return left and right
        return dfs(root, float("-inf"), float("inf"))
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(h)
<img width="1435" height="679" alt="image" src="https://github.com/user-attachments/assets/f33c27c7-6d65-4ce2-adbe-c72f716a519d" />

              
