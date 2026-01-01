[Question](https://leetcode.com/problems/maximum-subarray/description/?envType=problem-list-v2&envId=array)


## Implementation
Optimal solution
```python
class Solution(object):
    def maxSubArray(self, nums):
        currentSum = nums[0]
        maxSum = nums[0]
        for i in range(1, len(nums)):
            currentSum = max(nums[i], currentSum + nums[i])
            maxSum = max(maxSum, currentSum)
        return maxSum
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)

<img width="2527" height="990" alt="image" src="https://github.com/user-attachments/assets/745520d6-c4e5-4e19-a43e-bd4da03a48d2" />
