[Question](https://leetcode.com/problems/next-permutation/description/?envType=problem-list-v2&envId=array)


## Implementation
Optimal solution
```python
class Solution(object):
    def nextPermutation(self, nums):
        n = len(nums)
        j = n - 2
        while j >= 0 and nums[j] >= nums[j + 1]:
            j -= 1
        if j >= 0:
            i = n - 1
            while nums[i] <= nums[j]:
                i -= 1
            nums[j], nums[i] = nums[i], nums[j]

        i, j = j + 1, n - 1
        while i < j:
            nums[i], nums[j] = nums[j], nums[i]
            i += 1
            j -= 1
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)

<img width="2526" height="933" alt="image" src="https://github.com/user-attachments/assets/61064b28-b24a-432f-96b6-efaee43182b1" />
