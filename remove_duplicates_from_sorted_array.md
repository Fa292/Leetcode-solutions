[Question](https://leetcode.com/problems/remove-duplicates-from-sorted-array/description/?envType=problem-list-v2&envId=two-pointers)


## Implementation
Optimal solution
```python
class Solution(object):
    def removeDuplicates(self, nums):
        k = 1
        for i in range(1, len(nums)):
            if nums[i] != nums[i - 1]:
                nums[k] = nums[i]
                k += 1
                
        return k
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2520" height="939" alt="image" src="https://github.com/user-attachments/assets/5adf82a1-b83a-4359-872e-dcb10859c278" />
