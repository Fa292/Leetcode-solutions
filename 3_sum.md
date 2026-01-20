[Question](https://leetcode.com/problems/3sum/description/?envType=problem-list-v2&envId=two-pointers)


## Implementation
Optimal solution
```python
class Solution(object):
    
    def threeSum(self, nums):
        nums.sort()
        res = []
        n = len(nums)

        for i in range(n):
            
            if i > 0 and nums[i] == nums[i - 1]:
                continue

            left, right = i + 1, n - 1

            while left < right:
                total = nums[i] + nums[left] + nums[right]

                if total == 0:
                    res.append([nums[i], nums[left], nums[right]])

                    left += 1
                    right -= 1

                    
                    while left < right and nums[left] == nums[left - 1]:
                        left += 1
                    while left < right and nums[right] == nums[right + 1]:
                        right -= 1

                elif total < 0:
                    left += 1
                else:
                    right -= 1

        return res
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2501" height="932" alt="image" src="https://github.com/user-attachments/assets/86aa6d8a-9a36-40a7-8303-f8f92e0ac087" />
