[Question](https://leetcode.com/problems/find-the-index-of-the-first-occurrence-in-a-string/description/?envType=problem-list-v2&envId=string)


## Implementation
Optimal solution
```python
class Solution(object):
    def strStr(self, haystack, needle):
        
        n = len(needle)
        m = len(haystack)
        for i in range(m - n + 1):
            j = 0
            while j < n and haystack[i + j] == needle[j]:
                j += 1
            if j == n:
                return i
        return -1
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2513" height="923" alt="image" src="https://github.com/user-attachments/assets/07832f81-24b8-4185-98ec-66bd42fe817e" />
