[Question](https://leetcode.com/problems/copy-list-with-random-pointer/description/)


## Implementation
Optimal solution
```python
def copyRandomList(self, head):
        if not head:
            return head
        hash = {}
        old = head
        while old:
            copy = Node(old.val)
            hash[old] = copy
            old = old.next
        curr = head
        
        while curr:
            copy = hash[curr]
            copy.next = hash.get(curr.next)
            copy.random = hash.get(curr.random)
            curr = curr.next
        return hash[head]
```
## Complexities
- Time complexity: O(n)
- Space complexity: O(n)
<img width="2549" height="1106" alt="image" src="https://github.com/user-attachments/assets/b4a7c3dd-3101-4198-b1d8-c854474382a3" />
