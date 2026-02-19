[Question](https://leetcode.com/problems/contiguous-array/description/?envType=problem-list-v2&envId=prefix-sum)


## Implementation
Optimal solution
```python
class Solution(object):
    def findMaxLength(self, nums):
        prefix_sum = 0
        hash = {0: -1}
        max_length = 0
        for i in range(len(nums)):
            if nums[i] == 0:
                prefix_sum -= 1
            else:
                prefix_sum += 1
            if prefix_sum in hash:
                length = i - hash[prefix_sum]
                max_length = max(length, max_length)
            else:
                hash[prefix_sum] = i
        return max_length
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(n)
<img width="2504" height="951" alt="image" src="https://github.com/user-attachments/assets/20842aef-712d-4139-a95f-84554da9fa8e" />
