---
published : true

title : "Python Errors"
permalink : "/py/errors"
layout : note
excerpt : "Errors I stumbled upon"

alias : 
categories : ["py"]
tags : 

# date : 2022-04-14 00:00:00 +0000

showfooter : 
showgraph : 
---

## ValueError 
### ValueError: max() arg is an empty sequence | ValueError: min() arg is an empty sequence
- Error Caused : by python's [[py.func.max|max()]] and [[py.func.min|min()]]method as requires non empty sequence

```python
myDic = {}
if not myDic: 
	x = 69
else:
	x = max(myDic)
``` 
---

Return to [[py.python|python]]

---
