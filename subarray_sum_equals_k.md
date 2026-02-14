[Question](https://leetcode.com/problems/subarray-sum-equals-k/description/?envType=problem-list-v2&envId=hash-table)


## Implementation
Optimal solution
```python
class Solution(object):
    def subarraySum(self, nums, k):
        
        count = 0
        prefixSum = 0
        hash = {0: 1}
        for num in nums:
            prefixSum += num
            if prefixSum - k in hash:
                count += hash[prefixSum - k]
            hash[prefixSum] = hash.get(prefixSum, 0) + 1
        return count
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(n)
<img width="2506" height="936" alt="image" src="https://github.com/user-attachments/assets/e82c0fbb-ad26-4299-812c-e2d29b954c6f" />
