[Question](https://leetcode.com/problems/binary-tree-inorder-traversal/description/)


## Implementation
Optimal solution
```python
def inorderTraversal(self, root):
        elem = []
        def inorder(root):
            if root is None:
                return 
            
            inorder(root.left)
            elem.append(root.val)
            
            inorder(root.right)
        inorder(root)
        return elem
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(h)
<img width="2542" height="949" alt="image" src="https://github.com/user-attachments/assets/b8672af6-9baf-40ca-b3c3-a7766afb49bc" />
