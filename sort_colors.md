[Question](https://leetcode.com/problems/sort-colors/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def sortColors(self, nums):
        
        i = j = 0
        
        k = len(nums) - 1
        while j <= k:
            if nums[j] == 0:
                nums[i], nums[j] = nums[j], nums[i]
                i += 1
                j += 1
            elif nums[j] == 1:
                j += 1
            else:
                nums[j], nums[k] = nums[k], nums[j]
                k -= 1
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2491" height="932" alt="image" src="https://github.com/user-attachments/assets/2f91a8d2-6b88-4139-b679-7e2317798298" />
