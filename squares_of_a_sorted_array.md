[Question](https://leetcode.com/problems/squares-of-a-sorted-array/description/?envType=problem-list-v2&envId=two-pointers)


## Implementation
Optimal solution
```python
class Solution(object):
    def sortedSquares(self, nums):
        n = len(nums)
        left = 0
        right = n - 1
        result = [0] * n
        pos = n - 1
        while left <= right:
            if abs(nums[left]) < abs(nums[right]):
                result[pos] = nums[right] ** 2
                right -= 1
            else:
                result[pos] = nums[left] ** 2
                left += 1
            pos -= 1
        return result
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(n)
<img width="2505" height="929" alt="image" src="https://github.com/user-attachments/assets/539ee9ea-b1c0-481f-8ae5-87518832b191" />
