[Question](https://leetcode.com/problems/plus-one/description/?envType=problem-list-v2&envId=array)


## Implementation
Optimal solution
```python
class Solution(object):
    def plusOne(self, digits):
        n = len(digits)

        for i in range(n - 1, -1, -1):
            if digits[i] < 9:
                digits[i] += 1
                return digits
            digits[i] = 0

        return [1] + digits
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1) ignoring output array

<img width="2525" height="936" alt="image" src="https://github.com/user-attachments/assets/cf699c75-cc1c-43fd-8d45-6c23a6a3c9d3" />
