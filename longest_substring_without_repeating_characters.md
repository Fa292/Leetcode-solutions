[Question](https://leetcode.com/problems/longest-substring-without-repeating-characters/description/?envType=problem-list-v2&envId=string)


## Implementation
Optimal solution
```python
class Solution(object):
    def lengthOfLongestSubstring(self, s):
        seen = set()
        left = 0
        max_len = 0
        for right in range(len(s)):
            while s[right] in seen:
                seen.remove(s[left])
                left += 1

            seen.add(s[right])
            max_len = max(max_len, right - left + 1)
        return max_len
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2511" height="977" alt="image" src="https://github.com/user-attachments/assets/d675f2a2-db8b-42d5-9646-55ec874c2540" />
