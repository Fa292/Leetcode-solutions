[Question](https://leetcode.com/problems/minimum-size-subarray-sum/description/?envType=problem-list-v2&envId=sliding-window)


## Implementation
Optimal solution
```python
class Solution(object):
    def minSubArrayLen(self, target, nums):
        min_len = float("inf")
        currSum = 0
        left = 0
        for right in range(len(nums)):
            
            currSum += nums[right]
            while currSum >= target:
                min_len = min(min_len, (right - left) + 1)
                currSum -= nums[left]
                left += 1
        return 0 if min_len == float("inf") else min_len
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2494" height="935" alt="image" src="https://github.com/user-attachments/assets/31b93484-63c1-4420-91f3-2e688166270c" />

