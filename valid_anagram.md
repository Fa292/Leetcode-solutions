[Question](https://leetcode.com/problems/valid-anagram/description/?envType=problem-list-v2&envId=string)


## Implementation
Optimal solution
```python
class Solution(object):
    def isAnagram(self, s, t):
        count = {}
        if len(s) != len(t):
            return False
        for c in s:
            if c in count:
                count[c] += 1
            else:
                count[c] = 1
        for c in t:
            if c not in count:
                return False
            else:
                if count[c] == 0:
                    return False
                count[c] -= 1
        return True
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(n)

<img width="2539" height="941" alt="image" src="https://github.com/user-attachments/assets/e59a7107-3ba3-45de-a193-bf8a71a7b6fc" />
