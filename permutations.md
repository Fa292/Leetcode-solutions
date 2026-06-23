[Question](https://leetcode.com/problems/permutations/description/)


## Implementation
Optimal solution
```python
def permute(self, nums):
        ans = [[]]
        for num in nums:
            new_ans = []
            for perm in ans:
                for i in range(len(perm) + 1):
                    new_perm = perm[:]
                    new_perm.insert(i, num)
                    new_ans.append(new_perm)
            ans = new_ans
        return ans
```

## Complexities
- Time complexity: O(n * n!)
- Space complexity: O(n * n!)
<img width="2538" height="1005" alt="image" src="https://github.com/user-attachments/assets/64d5e150-58cc-4e43-95a7-d8ddf09c8fa9" />
