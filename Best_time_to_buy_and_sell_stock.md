[Question](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/description/?envType=problem-list-v2&envId=array)


## Implementation
Optimal solution
```python
class Solution(object):
    def maxProfit(self, prices):
        min_price = float("inf")
        max_profit = 0
        for price in prices:
            if price < min_price:
                min_price = price
            elif price - min_price > max_profit:
                max_profit = price - min_price
        return max_profit
```

## Complexities
- Time complexity: O(n)
- Space complexity: O(1)

<img width="2555" height="969" alt="image" src="https://github.com/user-attachments/assets/95f56f2b-1d40-4d3f-ac68-51977b4bfab6" />


