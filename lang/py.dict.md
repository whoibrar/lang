---
published : true

title : 
permalink : "/py/dic"
layout : note
excerpt : 

alias : 
categories : ["py"]
tags : 

# date : 2022-05-28 00:00:00 +0000

showfooter : 
showgraph : 
created_at: 2022-06-09 21:45:38 +0530
modified_at: 2022-06-09 21:45:38 +0530
---

## Quick Tricks

### Make a Frequency mapping of array elements

```python

nums = [1,2,2,1,1,3,4,4,4,4,4,5,0]

mydic = {}
mydic[i]=mydic.get(i,0)+1 
# adds key with val 0 if not present

mydic[i]=mydic[i]+1
# error if key not present

```

