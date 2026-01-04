[Question](https://leetcode.com/problems/two-sum/description/?envType=problem-list-v2&envId=array)


## Implementation
Optimal solution
```python
class Solution(object):
    def twoSum(self, nums, target):
        lookup = {}
        for i, num in enumerate(nums):
            diff = target - num
            if diff in lookup:
                return [lookup[diff], i]
            lookup[num] = i
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(n)

<img width="2511" height="937" alt="image" src="https://github.com/user-attachments/assets/38ac5d1a-b5bc-4e71-bc46-6175df716f37" />
