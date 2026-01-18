[Question](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/description/?envType=problem-list-v2&envId=two-pointers)


## Implementation
Optimal solution
```python
class Solution(object):
    def twoSum(self, numbers, target):
        i = 0
        j = len(numbers) - 1
        while i < j:
            if numbers[i] + numbers[j] == target:
                return [i + 1, j + 1]
            elif numbers[i] + numbers[j] > target:
                j -= 1
            else:
                i += 1
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2515" height="1007" alt="image" src="https://github.com/user-attachments/assets/22849577-0337-4db0-9186-bf47c85c447d" />
