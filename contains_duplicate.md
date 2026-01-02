[Question](https://leetcode.com/problems/contains-duplicate/description/?envType=problem-list-v2&envId=array)


## Implementation
Optimal solution
```python
class Solution(object):
    def containsDuplicate(self, nums):
        return len(nums) != len(set(nums))
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(n)

<img width="2516" height="979" alt="image" src="https://github.com/user-attachments/assets/12ed9080-5b0d-4a29-b049-8590c93d5c65" />
