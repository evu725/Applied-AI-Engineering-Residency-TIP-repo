# Day 3
Problem: Reverse String
Leetcode link: https://leetcode.com/problems/reverse-string/

Input: A string
Output: A integer that is the length of longest substring without duplicate charcaters

Algorithm:
```js
function reverseString(s) {
    let left = 0;
    let right = s.length - 1;
    while (left < right) {
        let temp = s[left];
        s[left] = s[right];
        s[right] = temp;
    }
}
```
Python Solution:
```python
class Solution:
    def reverseString(self, s: List[str]) -> None:
        """
        Do not return anything, modify s in-place instead.
        """
        left = 0
        right = len(s) - 1

        while (left < right):
            temp = s[left]
            s[left] = s[right]
            s[right] = temp
            left+=1
            right-=1

        return s
        
```

Problem: Longest Substring Without Repeating Characters
Leetcode link: https://leetcode.com/problems/longest-substring-without-repeating-characters/description/

Input: A string
Output: A integer that is the length of longest substring without duplicate charcaters

Algorithm:
```js
function lengthOfLongestSubstring(s) {
    let seen = {};
    let left = 0;
    let maxLength = 0;
    for (let right = 0; right < s.length; right++) {
        if (seen[s[right]] !== undefined && seen[s[right]] >= left) {
            left = seen[s[right]] + 1;
        }
        seen[s[right]] = right;
        maxLength = Math.max(maxLength, right - left + 1);
    }
    return maxLength;
}
```

//strongly typed
```python
class Solution:
    def lengthOfLongestSubstring(self, s: str) -> int:
        seen = {}
        left = 0
        max_length = 0
        for right in range(len(s)):
            if s[right] in seen and seen[s[right]] >= left:
                left = seen[s[right]] + 1

            seen[s[right]] = right
            max_length = max(max_length, right - left + 1)

        return max_length
```
