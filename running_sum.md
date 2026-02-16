[Question](https://leetcode.com/problems/running-sum-of-1d-array/description/?envType=problem-list-v2&envId=prefix-sum)


## Implementation
Optimal solution
```python
class Solution(object):
    def runningSum(self, nums):
        
        
        for i in range(1, len(nums)):
            nums[i] = nums[i - 1] + nums[i]
        return nums
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2512" height="1006" alt="image" src="https://github.com/user-attachments/assets/fcd77fc5-a55b-4f3c-952d-5eb2d909d85a" />
