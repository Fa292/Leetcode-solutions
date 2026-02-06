[Question](https://leetcode.com/problems/max-consecutive-ones-iii/description/?envType=problem-list-v2&envId=sliding-window)


## Implementation
Optimal solution
```python
class Solution(object):
    def longestOnes(self, nums, k):
        left = 0
        zeros = 0
        max_len = 0
        for right in range(len(nums)):
            if nums[right] == 0:
                zeros += 1
            
            while zeros > k:
                if nums[left] == 0:
                    zeros -= 1
                left += 1
            max_len = max(max_len, right - left + 1)
        return max_len
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2516" height="1002" alt="image" src="https://github.com/user-attachments/assets/18179e73-c2a8-4978-9281-97ef1600ef5d" />
