[Question](https://leetcode.com/problems/corporate-flight-bookings/description/?envType=problem-list-v2&envId=prefix-sum)


## Implementation
Optimal solution
```python
class Solution(object):
    def corpFlightBookings(self, bookings, n):
        output = [0] * n
        for start, end, seats in bookings:
            output[start - 1] += seats
            if end < n:   
                output[end] -= seats
        curr = 0
        for i in range(len(output)):
            curr += output[i]
            output[i] = curr
            
        return output
```

## Complexities
- Time complexity: O(n + m)
- Space complexity: O(n)
<img width="2513" height="937" alt="image" src="https://github.com/user-attachments/assets/c1b3e38c-f6d7-43c7-963d-585fe3e08222" />
