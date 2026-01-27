[Question](https://leetcode.com/problems/intersection-of-two-arrays/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def intersection(self, nums1, nums2):
        set_nums2 = set(nums2)
        common = set()
        for num in nums1:
            
            if num in set_nums2:
                common.add(num)
        return list(common)
```

## Complexities
- Time complexity: O(m + n)
- Space complexity: O(m + n)
<img width="2500" height="929" alt="image" src="https://github.com/user-attachments/assets/414e7359-603c-471f-9045-691f643f2513" />


