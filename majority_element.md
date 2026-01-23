[Question](https://leetcode.com/problems/majority-element/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def majorityElement(self, nums):
        majority = res = 0
        for n in nums:
            if majority == 0:
                res = n
            majority += 1 if n == res else -1
        return res
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2504" height="932" alt="image" src="https://github.com/user-attachments/assets/abb1f358-9466-4d10-97a6-3faa8613edfe" />
