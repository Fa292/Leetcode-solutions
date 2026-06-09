[Question](https://leetcode.com/problems/min-stack/description/?envType=problem-list-v2&envId=stack)


## Implementation
Optimal solution
```python
class MinStack(object):

    def __init__(self):
        self.stack = []
        self.minstack = []
        

    def push(self, value):
        self.stack.append(value)
        if not self.minstack:
            self.minstack.append(value)
        else:
            self.minstack.append(min(value, self.minstack[-1]))
        

    def pop(self):
        
        self.stack.pop()
        self.minstack.pop()
        

    def top(self):
        return self.stack[-1]
        

    def getMin(self):
        return self.minstack[-1]
```

## Complexities
- Time complexity: O(1)
- Space complexity: O(n)
<img width="2554" height="939" alt="image" src="https://github.com/user-attachments/assets/e82327c8-11fb-4211-94c7-0660368bd47a" />


