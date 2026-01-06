[Question](https://leetcode.com/problems/move-zeroes/description/?envType=problem-list-v2&envId=array)


## Implementation
Optimal solution
```python
class Solution(object):
    def moveZeroes(self, nums):
        last_index = 0
        n = len(nums)
        for i in range(n):
            if nums[i] != 0:
                nums[last_index] = nums[i]
                last_index += 1
        for i in range(last_index, n):
            nums[i] = 0
        return nums
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)

<img width="2535" height="936" alt="image" src="https://github.com/user-attachments/assets/a53ca62c-5f57-44d9-b1b5-5b46871718d1" />
