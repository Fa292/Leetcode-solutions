[Question](https://leetcode.com/problems/binary-tree-preorder-traversal/description/)


## Implementation
Optimal solution
```python
def postorderTraversal(self, root):
        stack = []
        elem = []
        lastVisited = None
        while root or stack:
            while root:
                stack.append(root)
                root = root.left
            peek = stack[-1]
            if peek.right and lastVisited != peek.right:
                root = peek.right
            else:
                elem.append(peek.val)
                lastVisited = stack.pop()
        return elem
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(h)
<img width="2550" height="1014" alt="image" src="https://github.com/user-attachments/assets/fb6e305c-e45c-414a-990e-202562a642de" />
