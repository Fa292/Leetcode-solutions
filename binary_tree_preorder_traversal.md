[Question](https://leetcode.com/problems/binary-tree-preorder-traversal/description/)


## Implementation
Optimal solution
```python
def preorderTraversal(self, root):
        stack = []
        elem = []
        while root or stack:
            while root:
                stack.append(root)
                elem.append(root.val)
                root = root.left
            root = stack.pop()
            root = root.right
        return elem
```

## Complexities
- Time complexity: O(h)
- Space complexity: O(h)
<img width="2552" height="1006" alt="image" src="https://github.com/user-attachments/assets/c2670111-186b-4029-8cc0-db4de40e802e" />
