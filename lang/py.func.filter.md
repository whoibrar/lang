---
published : true

title : "Python filter()"
permalink : "/py/func/filter"
layout : note
excerpt : 

alias : "filter()"
categories : ["py"]
tags : 

# date : 2022-04-15 00:00:00 +0000

showfooter : 
showgraph : 
---

- Summary 
	- Apply a given `func` filter over a sequence
- Syntax
	- `filter(myFunc, mySequence)`
	- Parameters
		- function
			- that which evaluates to Boolean
		- sequence
			- sets, lists, tuples, or containers of iterators

```python
# function that filters vowels
def fun(variable):
    letters = ['a', 'e', 'i', 'o', 'u']
    if (variable in letters):
        return True
    else:
        return False

# sequence
sequence = ['g', 'e', 'e', 'j', 'k', 's', 'p', 'r']
  
# using filter function
filtered = filter(fun, sequence)
```

---

Return to [[py.python|python]]

---
