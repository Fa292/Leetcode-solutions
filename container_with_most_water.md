[Question](https://leetcode.com/problems/container-with-most-water/description/?envType=problem-list-v2&envId=two-pointers)


## Implementation
Optimal solution
```python
class Solution(object):
    def maxArea(self, height):
        i = 0
        n  = len(height)
        j = n - 1
        maxArea = 0
        while i < j:
            area = min(height[i], height[j]) * (j - i)
            maxArea = max(area, maxArea)
            if height[i] < height[j]:
                i += 1
            else:
                j -= 1
        return maxArea
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)

<img width="2507" height="940" alt="image" src="https://github.com/user-attachments/assets/1857dc39-abea-4131-9852-b3752640392a" />
