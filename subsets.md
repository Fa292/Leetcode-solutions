[Question](https://leetcode.com/problems/subsets/description/)


## Implementation
Optimal solution
```python
def subsets(self, nums):
        ans = [[]]

        for num in nums:
            subsets = []
            for subs in ans:
                new = subs[:]
                new.append(num)
                subsets.append(new)
            ans.extend(subsets)    
            
        return ans
```

## Complexities
- Time complexity: O(n * 2^n)
- Space complexity: O(n * 2^n)
<img width="2534" height="1003" alt="image" src="https://github.com/user-attachments/assets/c408c62e-72b4-41c8-b7c1-503b73799197" />
