## Difficulty: `Easy`

Given two strings `s` and `t`, return `true` if the two strings are anagrams of each other, otherwise return `false`.

An **anagram** is a string that contains the exact same characters as another string, but the order of the characters can be different.

**Example 1:**

```java
Input: s = "racecar", t = "carrace"

Output: true
```

Copy

**Example 2:**

```java
Input: s = "jar", t = "jam"

Output: false
```

Copy

**Constraints:**

- `s` and `t` consist of lowercase English letters.
---
## Solution:
```python
class Solution:
	def isAnagram(self, s: str, t: str) -> bool:
		s_dict = dict()
		t_dict = dict()
		for i, v in enumerate(s):
			if v in s_dict.keys():
				s_dict[v] += 1
			else:
				s_dict[v] = 1
				
		for i, v in enumerate(t):
			if v in t_dict.keys():
				t_dict[v] += 1
			else:
				t_dict[v] = 1
				
		if s_dict == t_dict:
			return True
		else:
			return False
```