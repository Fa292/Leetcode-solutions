[Question](https://leetcode.com/problems/find-all-numbers-disappeared-in-an-array/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def findDisappearedNumbers(self, nums):
        for i in range(len(nums)):
            idx = abs(nums[i]) - 1
            if nums[idx] > 0:
                nums[idx] *= -1
        res = []
        for i in range(len(nums)):
            if nums[i] > 0:
                res.append(i + 1)
        return res
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2526" height="930" alt="image" src="https://github.com/user-attachments/assets/d5bdc043-2e3d-4902-8c3d-73ae481043dc" />
