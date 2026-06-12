# Day 2
```python
class Solution:
    def maxProfit(self, prices: List[int]) -> int:
        minPrice = inf
        maxProfit = 0
        for price in prices:
            if price < minPrice:
                minPrice = price
            elif price - minPrice > maxProfit:
                maxProfit = price - minPrice
                
        return maxProfit
```
