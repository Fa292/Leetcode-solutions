[Question](https://leetcode.com/problems/path-sum/description/)


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
<img width="2535" height="1020" alt="image" src="https://github.com/user-attachments/assets/3d844e4e-159d-48ea-81ed-31ee16ba4bab" />
