# Day 7
Problem: Single Number
Leetcode link: https://leetcode.com/problems/single-number/

Input: a non-empty list of integers
Output: a unique integer that appears only once
Algorithm:
```python
class Solution:
    def singleNumber(self, nums: List[int]) -> int:
        """
        Find the number that appears exactly once.
        """

        counts = {}

        # count occurrences of each number
        for i in nums:
            if i in counts:
                counts[i] += 1
            else:
                counts[i] = 1

        # return the number with the smallest frequency
        return min(counts, key=counts.get)
```