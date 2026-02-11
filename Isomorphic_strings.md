[Question](https://leetcode.com/problems/isomorphic-strings/description/?envType=problem-list-v2&envId=hash-table)


## Implementation
Optimal solution
```python
class Solution(object):
    def isIsomorphic(self, s, t):
        hash_s = {}
        hash_t = {}
        for i in range(len(s)):       
            c1 = s[i]
            c2 = t[i]
            if c1 in hash_s and c2 != hash_s[c1]:
                return False
            if c2 in hash_t and c1 != hash_t[c2]:
                return False
            
            hash_s[s[i]] = t[i]
            hash_t[t[i]] = s[i]
        return True
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2514" height="938" alt="image" src="https://github.com/user-attachments/assets/9393922b-e388-47ff-b0f8-3be6abd67ef4" />
