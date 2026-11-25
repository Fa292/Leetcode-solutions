[Question](https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/description/)


## Implementation
Optimal solution
```python
def buildTree(self, preorder: list[int], inorder: list[int]) -> TreeNode | None:
        in_map = {num: i for i, num in enumerate(inorder)}
        pre_idx = 0
        def dfs(left, right):
            nonlocal pre_idx
            if left > right:
                return None
            root_val = preorder[pre_idx]
            pre_idx += 1
            root = TreeNode(root_val)
            mid = in_map[root_val]
            root.left = dfs(left, mid - 1)
            root.right = dfs(mid + 1, right)
            return root
        return dfs(0, len(inorder) - 1)
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(n)
<img width="1440" height="731" alt="image" src="https://github.com/user-attachments/assets/479dedb5-6278-4ffb-b1d7-7bd0de09cc95" />
