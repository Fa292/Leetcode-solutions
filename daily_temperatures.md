[Question](https://leetcode.com/problems/daily-temperatures/description/?envType=problem-list-v2&envId=stack)


## Implementation
Optimal solution
```python
def dailyTemperatures(self, temperatures):
        

        stack = []
        size = len(temperatures)
        ans = [0] * size
        for i in range(size):
            while stack and temperatures[i] > temperatures[stack[-1]]:
                idx = stack.pop()
                ans[idx] = i - idx
            stack.append(i)
        return ans
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(n)
<img width="2545" height="930" alt="image" src="https://github.com/user-attachments/assets/8e2084f8-a2fa-4087-b5b8-a54167edbe78" />
