---
published : true

title : Python Tuples
permalink : "/py/tuples"
layout : note
excerpt : 

alias : ["Python Tuples"]
categories : 
tags : 

# date : 2022-04-14 00:00:00 +0000

showfooter : 
showgraph : 
---

### Tuples Comparison
- Two tuples can be compared by comparing their elements starting from first. 
- If there is a tie (elements are equal), the second element is compared, and so on.
```python
>>> (1,3) > (1, 4)
False
>>> (1, 4) < (2,2)
True
>>> (1, 4, 1) < (2, 1)
True
```

---

Return to [[py.python|python]]

---
