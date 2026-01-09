[Question](https://leetcode.com/problems/first-unique-character-in-a-string/description/?envType=problem-list-v2&envId=string)


## Implementation
Optimal solution
```python
class Solution(object):
    def firstUniqChar(self, s):
        count = [0] * 26
        for c in s:
            count[ord(c) - ord('a')] += 1
        for i, c in enumerate(s):
            if count[ord(c) - ord('a')] == 1:
                return i
        return -1
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2544" height="934" alt="image" src="https://github.com/user-attachments/assets/14e3da28-c21b-4324-9652-f9834ed4950a" />
