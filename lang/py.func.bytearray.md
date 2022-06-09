---
published : true

title : "Python bytearray()"
permalink : "/py/func/bytearray"
layout : note
excerpt : 

alias : "bytearray()"
categories : ["py"]
tags : 

# date : 2022-04-15 00:00:00 +0000

showfooter : 
showgraph : 
created_at: 2022-06-04 01:26:21 +0530
last_modified_at: 2022-06-04 01:26:21 +0530
---

modified yet ? yes ?

- Summary 
	- returns a bytearray object which is an array of the given bytes
	- it is mutable sequence of integers in the range `0 <= x < 256`
- Syntax 
	- `bytearray([source[, encoding[, errors]]]) `
	- Parameters
		- source (Optional) - source to initialize the array of bytes.
			- How source works with different inputs
				- string → converts to byte using str.encode()
				- integer → array of given size initialized to null
				- iterable → array of size of len, initialized of iterables which must be integers b/w 0 and 256
		- encoding (Optional) 
			- if the source is a string, the encoding of the string.
		- errors (Optional)
			- if the source is a string, the action to take when the encoding conversion fails
- Return Value
	-  returns an array of bytes of the given size and initialization values.

```python

>>> print(bytearray(5))
>>> bytearray(b'\x00\x00\x00\x00\x00')

```

---

Return to [[py.python|python]]

---
