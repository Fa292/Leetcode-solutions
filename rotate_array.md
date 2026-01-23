[Question](https://leetcode.com/problems/rotate-array/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def rotate(self, nums, k):
        n = len(nums)
        k %= n
        nums[:] = nums[-k:] + nums[:-k]
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(n)
<img width="2485" height="927" alt="image" src="https://github.com/user-attachments/assets/21dcdfee-f101-41c2-9f65-b413caf4cad5" />
