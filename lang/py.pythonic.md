---
published : true

title : Pythonic Way
permalink : /py/pythonic
layout : note
excerpt : 

alias : 
categories : "py"
tags : 

# date : 2022-04-14 00:00:00 +0000

showfooter : 
showgraph : 
---


### Starting Counter with True instead of Zero
- [Number of Steps to Reduce a Number to Zero - LeetCode](https://leetcode.com/problems/number-of-steps-to-reduce-a-number-to-zero/)

```python

#The Code
if n==0: 
	return 0
else: 
	count = 0
	while n>0:
		#modify n
		count+=1
	return count-1

#The Pythonic Code
count=n==0
while n>0:
	#modifyn
	count+=1
return count-1

#How
## Staring with True, subtracting one will lead to false
```

---

Return to [[py.python|python]]

---
