[Question](https://leetcode.com/problems/valid-palindrome/description/?envType=problem-list-v2&envId=string)


## Implementation
Optimal solution
```python
class Solution(object):
    def isPalindrome(self, s):
        i, j = 0, len(s) - 1
        while i < j:
            if not s[i].isalnum():
                i += 1
                continue
            if not s[j].isalnum():
                j -= 1
                continue
            if s[i].lower() != s[j].lower():
                return False
            i += 1
            j -= 1
        return True
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2521" height="1020" alt="image" src="https://github.com/user-attachments/assets/ee3e022a-5478-44e5-b1c5-4510d797c5cf" />
