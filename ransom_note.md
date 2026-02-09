[Question](https://leetcode.com/problems/ransom-note/description/?envType=problem-list-v2&envId=hash-table)


## Implementation
Optimal solution
```python
class Solution(object):
    def canConstruct(self, ransomNote, magazine):
        if len(ransomNote) > len(magazine):
            return False
        hash = {}
        for char in magazine:
            hash[char] = hash.get(char, 0) + 1
        for char in ransomNote:
            if hash.get(char, 0) > 0:
                hash[char] -= 1
            else:
                return False
        return True
```

## Complexities
- Time complexity: O(n + m)
- Space complexity: O(1)
<img width="2501" height="941" alt="image" src="https://github.com/user-attachments/assets/46c4716a-85b8-4284-a2a7-958404d31a00" />
