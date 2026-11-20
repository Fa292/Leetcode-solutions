[Question](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/description/)


## Implementation
Optimal solution
```python
def lowestCommonAncestor(self, root: 'TreeNode', p: 'TreeNode', q: 'TreeNode') -> 'TreeNode':
        if not root:
            return root
        def dfs(root):
            if not root:
                return None
            if root == p or root == q:
                return root
            left = dfs(root.left)
            right = dfs(root.right)
            if left is not None and right is not None:
                return root
            return left or right
        return dfs(root)
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(h)
<img width="1430" height="768" alt="image" src="https://github.com/user-attachments/assets/10af5820-ec6f-4cfb-b267-93ff1a8ff7a2" />
