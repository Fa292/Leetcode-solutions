[Question](https://leetcode.com/problems/permutation-in-string/description/?envType=problem-list-v2&envId=sliding-window)


## Implementation
Optimal solution
```python
class Solution(object):
    def checkInclusion(self, s1, s2):
        len1 = len(s1)
        len2 = len(s2)

        if len1 > len2:
            return False

        count1 = [0] * 26
        count2 = [0] * 26

        
        for c in s1:
            count1[ord(c) - ord('a')] += 1

        left = 0

        for right in range(len2):
            
            count2[ord(s2[right]) - ord('a')] += 1

            
            if right - left + 1 > len1:
                count2[ord(s2[left]) - ord('a')] -= 1
                left += 1

            
            if count1 == count2:
                return True

        return False
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2508" height="925" alt="image" src="https://github.com/user-attachments/assets/ede11f83-f823-4447-a4c8-e60075917551" />
