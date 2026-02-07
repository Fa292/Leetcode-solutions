[Question](https://leetcode.com/problems/maximum-length-of-repeated-subarray/description/?envType=problem-list-v2&envId=sliding-window)


## Implementation
Optimal solution
```python
class Solution(object):
    
    def findLength(self, nums1, nums2):
        n, m = len(nums1), len(nums2)
        max_len = 0

        
        for i in range(n):
            curr = 0
            x, y = i, 0
            while x < n and y < m:
                if nums1[x] == nums2[y]:
                    curr += 1
                    max_len = max(max_len, curr)
                else:
                    curr = 0
                x += 1
                y += 1

        
        for j in range(1, m):
            curr = 0
            x, y = 0, j
            while x < n and y < m:
                if nums1[x] == nums2[y]:
                    curr += 1
                    max_len = max(max_len, curr)
                else:
                    curr = 0
                x += 1
                y += 1

        return max_len
```

## Complexities
- Time complexity: O(n * m)
- Space complexity: O(1)
<img width="2497" height="915" alt="image" src="https://github.com/user-attachments/assets/90395c46-4fd1-4958-8a0e-4b0d19028afb" />
