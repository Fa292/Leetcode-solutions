[Question](https://leetcode.com/problems/top-k-frequent-elements/description/?envType=problem-list-v2&envId=hash-table)


## Implementation
Optimal solution
```python
class Solution(object):
    def topKFrequent(self, nums, k):
        hash = {}
        for num in nums:
            hash[num] = hash.get(num, 0) + 1
        buckets = [[] for _ in range(len(nums) + 1)]
        for num, count in hash.items():
            buckets[count].append(num)
        output = []
        for i in range(len(buckets) - 1, 0, -1):
            for num in buckets[i]:
                output.append(num)
                if len(output) == k:
                    return output
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(n)
<img width="2506" height="943" alt="image" src="https://github.com/user-attachments/assets/57bf2e3a-c9ef-4666-a6a4-de2abe5169ce" />
