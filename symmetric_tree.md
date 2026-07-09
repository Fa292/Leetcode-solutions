[Question](https://leetcode.com/problems/symmetric-tree/description/)


## Implementation
Optimal solution
```python
def isSymmetric(self, root):
      stack = [(root.left, root.right)]
      while stack:
          left, right = stack.pop()
          if left is None and right is None:
              continue
          if left is None or right is None:
              return False
          if left.val != right.val:
              return False
          stack.append((left.left, right.right))
          stack.append((left.right, right.left))
      return True
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(h)
<img width="2543" height="956" alt="image" src="https://github.com/user-attachments/assets/6596e83b-7f41-430d-a8cc-f6a884a6fdcd" />
