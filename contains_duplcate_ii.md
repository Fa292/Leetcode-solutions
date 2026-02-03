[Question](https://leetcode.com/problems/contains-duplicate-ii/description/?envType=problem-list-v2&envId=sliding-window)


## Implementation
Optimal solution
```python
class Solution(object):
    def containsNearbyDuplicate(self, nums, k):
        lookup = {}
        for i, num in enumerate(nums):
            if num in lookup and abs(lookup[num] - i) <= k:
                return True
            else:
                lookup[num] = i
        return False
    
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(n)
<img width="2508" height="921" alt="image" src="https://github.com/user-attachments/assets/51b5f93c-4546-4568-9726-da0c08229613" />

