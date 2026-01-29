[Question](https://leetcode.com/problems/search-insert-position/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def searchInsert(self, nums, target):
        
        n = len(nums)
        left = 0
        right = n - 1
        while left <= right:
            mid_index = (left + right) // 2
            if nums[mid_index] == target:
                return mid_index
            elif nums[mid_index] < target:
                left = mid_index + 1
                
            else:
                right = mid_index - 1
        return left
```

## Complexities
- Time complexity: O(log n)
- Space complexity: O(1)
<img width="2537" height="933" alt="image" src="https://github.com/user-attachments/assets/f3b8dc9c-96e4-4127-98a2-87e937b9f75a" />
