[Question](https://leetcode.com/problems/car-pooling/description/?envType=problem-list-v2&envId=prefix-sum)


## Implementation
Optimal solution
```python
class Solution(object):
    def carPooling(self, trips, capacity):
        events = []
        for numPassengers, start, end in trips:
            events.append((start, numPassengers))
            events.append((end, -numPassengers))
        events.sort(key = lambda x: (x[0], x[1]))
        curr = 0
        for location, change in events:
            curr += change
            if curr > capacity:
                return False
        return True
```

## Complexities
- Time complexity: O(nlogn)
- Space complexity: O(n)
<img width="2512" height="944" alt="image" src="https://github.com/user-attachments/assets/5bd434b8-72fb-4792-8590-a50d48f3548c" />
