[Question](https://leetcode.com/problems/maximum-depth-of-binary-tree/description/)


## Implementation
Optimal solution
```python
def maxDepth(self, root):
      if root is None:
          return 0
      stack = [(root, 1)]
      ans = 0
      while stack:
          node, depth = stack.pop()
          ans = max(ans, depth)    
          if node.left:
              stack.append((node.left, depth + 1))
          if node.right:
              stack.append((node.right, depth + 1))
      return ans
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(h)
<img width="2548" height="953" alt="image" src="https://github.com/user-attachments/assets/8332efa6-d4ff-4308-8da6-46023de62fb7" />
