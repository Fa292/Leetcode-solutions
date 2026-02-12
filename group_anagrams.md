[Question](https://leetcode.com/problems/group-anagrams/description/?envType=problem-list-v2&envId=hash-table)


## Implementation
Optimal solution
```python
class Solution(object):
    def groupAnagrams(self, strs):
        hash = {}
        
        
        
        for s in strs:
            count = [0]*26
            for char in s:
                count[ord(char) - ord('a')] += 1
            key = tuple(count)
            hash.setdefault(key, []).append(s)           

        return list(hash.values())
```

## Complexities
- Time complexity: O(nk)
- Space complexity: O(nk)
<img width="2500" height="929" alt="image" src="https://github.com/user-attachments/assets/7f324eb8-eed9-4393-b1d1-d7b763d00e53" />
