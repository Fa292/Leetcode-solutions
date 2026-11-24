[Question](https://leetcode.com/problems/3sum/description/?envType=problem-list-v2&envId=two-pointers)


## Implementation
Optimal solution
```python
def insertIntoBST(self, root: TreeNode | None, val: int) -> TreeNode | None:
        
        
      def dfs(node):
          if not node:
              return TreeNode(val)
          if node.val < val:
              node.right = dfs(node.right)
          else:
              node.left = dfs(node.left)
          return node
      return dfs(root)
```

## Complexities
- Time complexity: O(h)
- Space complexity: O(h)
<img width="1333" height="776" alt="image" src="https://github.com/user-attachments/assets/657536bf-37ed-4085-9db2-1fbb5374db1a" />
