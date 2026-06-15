[Question](https://leetcode.com/problems/evaluate-reverse-polish-notation/description/?envType=problem-list-v2&envId=stack)


## Implementation
Optimal solution
```python
def evalRPN(self, tokens: List[str]) -> int:
        
        stack = []
        for i in range(len(tokens)):
            if tokens[i] == '+':
                a = stack.pop()
                b = stack.pop()
                stack.append(a + b)
            elif tokens[i] == "-":
                a = stack.pop()
                b = stack.pop()
                stack.append(b - a)
            elif tokens[i] == "*":
                a = stack.pop()
                b = stack.pop()
                stack.append(a * b)
            elif tokens[i] == "/":
                a = stack.pop()
                b = stack.pop()
                stack.append(int(b / a))
            else:
                stack.append(int(tokens[i]))
        return stack.pop()
        
```
## Complexities
- Time complexity: O(n)
- Space complexity: O(n)
<img width="2552" height="1099" alt="image" src="https://github.com/user-attachments/assets/28701192-aac9-4776-8284-3b31e6c2f044" />
