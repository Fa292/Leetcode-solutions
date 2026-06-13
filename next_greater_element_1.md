[Question](https://leetcode.com/problems/next-greater-element-i/description/?envType=problem-list-v2&envId=stack)


## Implementation
Optimal solution
```python
def nextGreaterElement(self, nums1, nums2):
        next_greater = {}
        stack = []
        for num in nums2:
            while stack and num > stack[-1]:
                prev = stack.pop()
                next_greater[prev] = num
            stack.append(num)
        for num in stack:
            next_greater[num] = -1
        output = [0] * len(nums1)
        for i in range(len(nums1)):
            output[i] = next_greater[nums1[i]]
        return output
        
```
## Complexities
- Time complexity: O(n)
- Space complexity: O(n)
<img width="2544" height="1007" alt="image" src="https://github.com/user-attachments/assets/66f0c2d4-c88f-4c9c-9caf-6020d724498e" />
