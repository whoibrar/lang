---
published : true

title : "Python Slicing"
permalink : "/py/slicing"
layout : note
excerpt : 

alias : ["Python Slicing"]
categories : "py"
tags : 

# date : 2022-04-14 00:00:00 +0000

showfooter : 
showgraph : 
---

### Basic Slicing

- Syntax 
	- `[start_at:stop_before:step]`
	- all three are optional arguments
- default values
	- `start_at = 0`
	- `stop_before = len(nums)`
	- `step = 1`

- Negative Values
	- Indexing
		- `-1` is 1st element from last
		- `-2` is 2nd element from last
	- Step value
		- sliced from reverse → end to start
		- needs start_at > stop_before

- Out of range → Empty lists
	- forgiving in a way that it doesn't throw any errors

### Slice Assignment
- The part of the list returned by the slice on the left-hand side of the expression is the part of the list that's going to be changed by slice assignment
- Syntax
	-  `myList[:3]=[a,b,c]` → replaces first three elements
- Insert elements without any replacing
	- `myList[i:i]=listBeInserted`
- Slice assignment with step
	- if `step` is not `1`, the inserted list must have the exact same length as that of the returned list slice, otherwise ValueError is thrown

```python

a=[1,2,3,4,5,6]

a[3:3]=['a','b','c'] → #[1,2,3,'a','b','c',4,5,6]
a[1:-2:2]=['p','q','r'] → #[1,'p','a','q','c','r',5,6]

```

### Basic slice [[vs]] slice assignment

```python

letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g']
letters[1:] = [ ] → #['a']

letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g']
print(letters[1:]) → #['b', 'c', 'd', 'e', 'f', 'g']

```

- **Basic Slicing** creates a new subsequence of the original sequence. You can assign this new sequence to a variable
- **Slice assignment** replaces the selected slice in the original sequence y with the value specified on the right-hand side of the equation

---

Return to [[py.python|python]]

---
