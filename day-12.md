# Day 12
Problem: Running Sum of 1d Array
Leetcode link: https://leetcode.com/problems/running-sum-of-1d-array/description/

```js
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var runningSum = function(nums) {

    let total_sum = 0;

    let arr = []
    for (let i = 0; i < nums.length; i++) {
        total_sum += nums[i];
        arr.push(total_sum);
    }
    return arr;
};
```


```python
class Solution:
    def runningSum(self, nums: List[int]) -> List[int]:
        # total sum
        total_sum = 0

        arr = []

        # loop through each number in the list
        for i in range(0, len(nums)):
            # increment every number
            total_sum += nums[i]
            arr.append(total_sum)

        return arr
```


Problem: Maximum Number of Vowels in a Substring of Given Length
Leetcode link: https://leetcode.com/problems/maximum-number-of-vowels-in-a-substring-of-given-length/description/


```python
class Solution:
    def maxVowels(self, s: str, k: int) -> int:
        # Input: a string
        # Output: maximum number of vowel letters in any substring
        # sliding window?
        vowels = {'a', 'e', 'i', 'o', 'u'}

        # get highest number of vowel letters
        total = 0
        top = 0
        # loop through the string
        for i in range(k, len(s)):
            # remove one char from left
            count -= 1
            # add one char to right
            top = max(top, total)
            pass
```
