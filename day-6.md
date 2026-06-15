# Day 6
Problem: Majority Element
Leetcode link: https://leetcode.com/problems/majority-element/description/

Input: An array of integers
Output: the majority element

Algorithm:
```python
class Solution:
    def majorityElement(self, nums: List[int]) -> int:
        count = {}

        for i in range(len(nums)):
            if nums[i] in count:
                count[nums[i]] += 1
            else:
                count[nums[i]] = 1

        return max(count, key=count.get)
```