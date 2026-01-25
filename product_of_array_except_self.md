[Question](https://leetcode.com/problems/product-of-array-except-self/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def productExceptSelf(self, nums):
        n = len(nums)
        output = [1] * n
        prefix = 1
        for i in range(n):
            output[i] = prefix
            prefix *= nums[i]
        suffix = 1
        for i in range(n - 1, -1, -1):
            output[i] *= suffix
            suffix *= nums[i]
        return output
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2503" height="921" alt="image" src="https://github.com/user-attachments/assets/0d950749-a174-422d-a3c4-7d2d95afa099" />
