[Question](https://leetcode.com/problems/longest-palindromic-substring/description/)


## Implementation
```python
def longestPalindrome(self, s):
        out = ""

        for i in range(len(s)):
            j = i
            k = i
            while j>= 0 and k < len(s) and s[j] == s[k]:
                if (k - j + 1) > len(out):
                    out = s[j: k + 1]
                j -= 1
                k += 1
            l = i
            m = i + 1
            while l>= 0 and m < len(s) and s[l] == s[m]:
                if (m - l + 1) > len(out):
                    out = s[l: m + 1]
                l -= 1
                m += 1
        return out
```
  ## Complexities
- Time complexity: O(n^2)
- Space complexity: O(1)
<img width="2559" height="1102" alt="image" src="https://github.com/user-attachments/assets/cc907def-8241-44a1-9ed3-38084f2482fb" />
