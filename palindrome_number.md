[Question](https://leetcode.com/problems/palindrome-number/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def isPalindrome(self, x):
        if x < 0:
            return False

        reverse = 0
        xcopy = x

        while x > 0:
            reverse = (reverse * 10) + (x % 10)
            x //= 10
        
        return reverse == xcopy
```

## Complexities
- Time complexity: O(logn)
- Space complexity: O(1)
<img width="2498" height="938" alt="image" src="https://github.com/user-attachments/assets/645f47dc-9b1d-47a2-8213-2f91e5f9a1bb" />
