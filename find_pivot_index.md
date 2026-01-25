[Question](https://leetcode.com/problems/find-pivot-index/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def pivotIndex(self, nums):
        left_sum = 0
        total = sum(nums)
        for i in range(len(nums)):
            right_sum = total - left_sum - nums[i]
            if left_sum == right_sum:
                return i
            left_sum += nums[i]
        return -1
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2513" height="939" alt="image" src="https://github.com/user-attachments/assets/260747f6-799d-4ac1-8b12-597d8cf72736" />
