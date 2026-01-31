[Question](https://leetcode.com/problems/length-of-last-word/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def lengthOfLastWord(self, s):
        output = 0
        for char in reversed(s):
            if char.isalpha():
                output += 1
            elif output != 0:
                return output
        return output
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2515" height="923" alt="image" src="https://github.com/user-attachments/assets/490985f0-0f77-4c62-a7eb-48d4ff5a4df5" />
