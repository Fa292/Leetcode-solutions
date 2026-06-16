[Question](https://leetcode.com/problems/fibonacci-number/description/?envType=problem-list-v2&envId=recursion)


## Implementation
Optimal solution
```python
def fib(self, n):
        if n > 1:
            return self.fib(n - 1) + self.fib(n - 2)
        else:
            return n
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2531" height="936" alt="image" src="https://github.com/user-attachments/assets/cf43140c-a596-4e23-8c93-b1855d5f5b47" />
