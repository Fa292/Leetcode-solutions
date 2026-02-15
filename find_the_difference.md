[Question](https://leetcode.com/problems/find-the-difference/description/?envType=problem-list-v2&envId=hash-table)


## Implementation
Optimal solution
```python
class Solution(object):
    def findTheDifference(self, s, t):
        hash = {}
        for char in s:
            hash[char] = hash.get(char, 0) + 1
        for char in t:
            if char not in hash or hash[char] == 0:
                return char
            hash[char] -= 1
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2512" height="1004" alt="image" src="https://github.com/user-attachments/assets/103b16b7-8638-485e-9680-d0241237e868" />
