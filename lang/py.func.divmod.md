---
published : true

title : "Python divmod()"
permalink : /py/func/divmod
layout : note
excerpt : 

alias: "divmod()"
categories : "py"
tags : 

# date : 2022-04-14 00:00:00 +0000

showfooter : 
showgraph : 
---


- Summary
	-  takes to numbers and returns tuple of quotient and remainder
	- If x and y are integers, the return value from `divmod()` is same as `(x // y, x % y)`.
- Syntax 
	- `divmod(x,y)`
	- Parameters
		- x → numerator
		- y → denomintator
		- both non-complex numbers

Code Snippets
```python

print('divmod(8, 3) = ', divmod(8, 3))
print('divmod(3, 8) = ', divmod(3, 8))
print('divmod(5, 5) = ', divmod(5, 5))

# divmod() with Floats
print('divmod(8.0, 3) = ', divmod(8.0, 3))
print('divmod(3, 8.0) = ', divmod(3, 8.0))
print('divmod(7.5, 2.5) = ', divmod(7.5, 2.5))
print('divmod(2.6, 0.5) = ', divmod(2.6, 0.5))

divmod(8, 3) =  (2, 2)
divmod(3, 8) =  (0, 3)
divmod(5, 5) =  (1, 0)
divmod(8.0, 3) =  (2.0, 2.0)
divmod(3, 8.0) =  (0.0, 3.0)
divmod(7.5, 2.5) =  (3.0, 0.0)
divmod(2.6, 0.5) =  (5.0, 0.10000000000000009)

```

---

Return to [[py.python|python]]

---
