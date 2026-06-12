# Day 4
```js
function groupAnagrams(strs) {
  const map = {};
  for (let i = 0; i < strs.length; i++) {
    const key = strs[i].split('').sort().join('');
    if (map[key] === undefined) {
      map[key] = [];
    }
    map[key].push(strs[i]);
  }
  return Object.values(map);
}
```

```python
class Solution:
    def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
      map = {}

      for s in strs:
          key = ''.join(sorted(s))
          if key not in map:
              map[key] = []
          map[key].append(s)

      return list(map.values())
```
