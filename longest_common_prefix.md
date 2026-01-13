[Question](https://leetcode.com/problems/longest-common-prefix/description/?envType=problem-list-v2&envId=string)


## Implementation
Optimal solution
```python
class Solution(object):
    def longestCommonPrefix(self, strs):
        if len(strs) == 0:
            return ""
        prefix = strs[0]
        for i in range(1, len(strs)):
            while strs[i].find(prefix) != 0:
                prefix = prefix[0 : len(prefix) - 1]
                if prefix == "":
                    return ""
        return prefix
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2522" height="931" alt="image" src="https://github.com/user-attachments/assets/f4a95dee-4641-4672-8137-ccafec48c07d" />
