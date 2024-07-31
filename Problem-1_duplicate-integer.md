## Difficulty: `Easy`
---
- Given an integer array `nums`, return `true` if any value appears **more than once** in the array, otherwise return `false`.
- **Example 1:**
```java
Input: nums = [1, 2, 3, 3]

Output: true
```
- Example 2:
```java
Input: nums = [1, 2, 3, 4]

Output: false
```
---
- Solution 1:
```python
class Solution:
	def hasDuplicate(self, nums: List[int]) -> bool:
		unique_set = set(nums)
		if len(nums) > len(unique_set):
			return True
		else:
			return False
```
---
- Solution 2:
```python
class Solution:
	def hasDuplicate(self, nums: List[int]) -> bool:
	thisDict = dict()
	if len(nums) < 1:
		return False
	for i,v in enumerate(nums):
		if v in thisDict.keys():
			thisDict[v] += 1
			return True
		else:
			thisDict[v] = 1
	return False
```