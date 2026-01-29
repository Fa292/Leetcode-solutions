[Question](https://leetcode.com/problems/pascals-triangle/description/)


## Implementation
Optimal solution
```python
class Solution(object):
    def generate(self, numRows):
        triangle = []
        for i in range(numRows):
            row = [1] * (i + 1)
            for j in range(1, i):
                row[j] = triangle[i - 1][j - 1] + triangle[i - 1][j]
            triangle.append(row)
        return triangle
```

## Complexities
- Time complexity: O(n^2)
- Space complexity: O(n^2)
<img width="2532" height="1001" alt="image" src="https://github.com/user-attachments/assets/5197feed-2edd-4aad-86af-8ade1d4cecd2" />
