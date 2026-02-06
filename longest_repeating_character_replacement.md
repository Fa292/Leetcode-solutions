[Question](https://leetcode.com/problems/longest-repeating-character-replacement/description/?envType=problem-list-v2&envId=sliding-window)


## Implementation
Optimal solution
```python
class Solution(object):
    def characterReplacement(self, s, k):
        freq = [0] * 26
        left = 0
        result = 0
        max_freq = 0
        for right in range(len(s)):
            idx = ord(s[right]) - ord('A')
            freq[idx] += 1
            max_freq = max(freq[idx], max_freq)
            while (right - left + 1) - max_freq > k:
                freq[ord(s[left]) - ord('A')] -= 1
                left += 1
            result = max(result, right - left + 1)
        return result
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2510" height="983" alt="image" src="https://github.com/user-attachments/assets/afdfa42c-1e33-488e-858f-0b42ec72e5b0" />
