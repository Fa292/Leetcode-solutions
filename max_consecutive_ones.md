[Question](https://leetcode.com/problems/max-consecutive-ones/description/)


## Implementation
```python
def findMaxConsecutiveOnes(self, nums):
        left = 0
        max_len = 0
        for right in range(len(nums)):
            if nums[right] == 0:
                left = right + 1
            max_len = max(max_len, right - left + 1)
        return max_len
```
  ## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2559" height="1100" alt="image" src="https://github.com/user-attachments/assets/5ac0f894-4fd8-4eec-8683-a92c54eb3f8e" />
