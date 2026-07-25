[Question](https://leetcode.com/problems/invert-binary-tree/description/)


## Implementation
Optimal solution
```python
def invertTree(self, root):
        if root is None:
            return None
        stack = [root]
        while stack:
            node = stack.pop()
            node.left, node.right = node.right, node.left
            if node.left:
                stack.append(node.left)
            if node.right:
                stack.append(node.right)
        return root
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(h)
<img width="2538" height="957" alt="image" src="https://github.com/user-attachments/assets/19cff8fb-a363-421a-82fd-772ab3e12207" />
