[Question](https://leetcode.com/problems/maximum-product-subarray/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def maxProduct(self, nums):
        currMax = nums[0]
        currMin = nums[0]
        maxProd = nums[0]
        for i in range(1, len(nums)):
            n = nums[i]
            tempMax = max(n, currMax * n, currMin * n)
            currMin = min(n, currMax * n, currMin * n)
            currMax = tempMax
            maxProd = max(maxProd, currMax)
        return maxProd
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2499" height="995" alt="image" src="https://github.com/user-attachments/assets/f334666a-db93-4530-9a7a-8e9be868d95b" />
