[Question](https://leetcode.com/problems/powx-n/description/?envType=problem-list-v2&envId=recursion)


## Implementation
Optimal solution
```python
def myPow(self, x, n):
        power = x
        if n < 0:
            x = 1 / x
            n = -n
        result = 1
        while n:
            if n % 2 == 1:
                result *= x
            x *= x
            n //= 2
        
        return result
```

## Complexities
- Time complexity: O(logn)
- Space complexity: O(1)
<img width="2559" height="1107" alt="image" src="https://github.com/user-attachments/assets/04d1a76c-190e-4124-af8e-053444a6e919" />
