[Question](https://leetcode.com/problems/find-the-highest-altitude/description/?envType=problem-list-v2&envId=prefix-sum)


## Implementation
Optimal solution
```python
class Solution(object):
    
    def largestAltitude(self, gain):
        maxNum = 0
        currSum = 0
        for num in gain:
            currSum += num
            maxNum = max(maxNum, currSum)
            
        return maxNum
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)
<img width="2513" height="940" alt="image" src="https://github.com/user-attachments/assets/1f2b87dc-0772-42c2-9ce1-f512e570687e" />
