[Question](https://leetcode.com/problems/implement-queue-using-stacks/description/?envType=problem-list-v2&envId=stack)


## Implementation
```python
class MyQueue(object):

    def __init__(self):
        self.stack = []
        self.stack2 = []

    def push(self, x):
        self.stack.append(x)
        

    def pop(self):
        if not self.stack2:
            while self.stack:
                self.stack2.append(self.stack.pop())
        return self.stack2.pop()

    def peek(self):
        if not self.stack2:
            while self.stack:
                self.stack2.append(self.stack.pop())
        return self.stack2[-1]
        

    def empty(self):
        return len(self.stack) == 0 and len(self.stack2) == 0
```

## Complexities
- Time complexity: O(1)
- Space complexity: O(n)
<img width="2543" height="1016" alt="image" src="https://github.com/user-attachments/assets/8f5b4a4b-1c5a-44e3-a4b7-6d6f6b80bf46" />
