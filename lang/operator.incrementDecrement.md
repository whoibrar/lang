---
published : true

title : "Increment Decrement Operator"
permalink : "/cs/operator/increment-decrement"
layout : note
excerpt : 

alias : 
categories : 
tags : 

created_at : 2022-04-18 00:00:00 +0000


created_at: 2022-04-18 05:30:00 +0530
modified_at: 2022-06-09 21:44:31 +0530
---

- `x++ x--` 
	- Post Increment / Decrement
	- First Use, then operation
- `++x --x`
	- Pre Increment / Decrement
	- First operation, then use
- Associativity
	- prefix ++ is R2L
	- postfix ++ is L2R
- Precedence
	- postfix > prefix
- [[CPP]] Special Case 
	- `x=x++; y=y--` doesn't change the value
	- `int x=5; x=x--;` still remains 5