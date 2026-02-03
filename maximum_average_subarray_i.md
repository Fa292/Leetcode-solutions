[Question](https://leetcode.com/problems/maximum-average-subarray-i/description/?envType=problem-list-v2&envId=sliding-window)


## Implementation
Optimal solution
```python
class Solution(object):
    def findMaxAverage(self, nums, k):
        
        j = 0
        curr_sum = 0
        maxAverage = float("-inf")
        for i in range(len(nums)):
            
            curr_sum += nums[i]
            if i >= (k -1):
                maxAverage = max(maxAverage, curr_sum/float(k))
                curr_sum -= nums[j]
                j += 1
            
            
        return maxAverage
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2512" height="905" alt="image" src="https://github.com/user-attachments/assets/08bc0d7a-4710-4cfb-8127-44083352c7a0" />
