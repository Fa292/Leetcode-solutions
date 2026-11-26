[Question](https://leetcode.com/problems/kth-smallest-element-in-a-bst/description/)


## Implementation
Optimal solution
```python
def kthSmallest(self, root: TreeNode | None, k: int) -> int:
        
        pos = 0

        def dfs(node):
            nonlocal pos

            if not node:
                return None

            left = dfs(node.left)
            if left is not None:
                return left

            pos += 1
            if pos == k:
                return node.val

            right = dfs(node.right)
            if right is not None:
                return right

            return None

        return dfs(root)
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(h)
<img width="1438" height="722" alt="image" src="https://github.com/user-attachments/assets/927d8fc3-e838-4365-8a6d-9659f9399e30" />
