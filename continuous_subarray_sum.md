[Question](https://leetcode.com/problems/continuous-subarray-sum/description/?envType=problem-list-v2&envId=prefix-sum)


## Implementation
Optimal solution
class Solution(object):
    def checkSubarraySum(self, nums, k):
        hash = {0: -1}
        prefix_sum = 0
        for i in range(len(nums)):
            prefix_sum += nums[i]
            remainder = prefix_sum % k
            if remainder in hash:
                if i - hash[remainder] >= 2:
                    return True
            else:
                hash[remainder] = i
        return False 
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(n)
<img width="2523" height="953" alt="image" src="https://github.com/user-attachments/assets/452b0154-4708-4d77-90a1-b0827210d0e0" />
