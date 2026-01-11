[Question](https://leetcode.com/problems/reverse-string/description/?envType=problem-list-v2&envId=string)


## Implementation
Optimal solution
```python
class Solution(object):
    def reverseString(self, s):
        n = len(s)
        i = 0
        j = n - 1
        while i < j:
            s[i], s[j] = s[j], s[i]
            i += 1
            j -= 1
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2511" height="936" alt="image" src="https://github.com/user-attachments/assets/24ce5cd5-9c0f-4d69-aa14-8520507bf1c0" />
