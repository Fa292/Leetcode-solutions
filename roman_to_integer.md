[Question](https://leetcode.com/problems/roman-to-integer/description/?envType=problem-list-v2&envId=hash-table)


## Implementation
Optimal solution
```python
class Solution(object):
    def romanToInt(self, s):
        hash = {'I': 1, 'V': 5, 'X': 10, 'L': 50, 'C': 100, 'D': 500, 'M': 1000}
        num = 0
        for i in range(len(s) - 1):
            if hash[s[i + 1]] > hash[s[i]]:
                num -= hash[s[i]]
            else:
                num += hash[s[i]]
        num += hash[s[-1]]
        return num
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2513" height="939" alt="image" src="https://github.com/user-attachments/assets/04c71c32-32e3-468a-a0ce-3521c131a75e" />

