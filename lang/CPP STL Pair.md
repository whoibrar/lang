---
published : true

title : "CPP STL Pair"
permalink : "/cpp/stl/pair"
layout : note
excerpt : 

alias : 
categories : "cpp"
tags : 

# date : 2022-05-16 00:00:00 +0000

showfooter : 
showgraph : 
created_at: 2022-06-08 17:56:58 +0530
modified_at: 2022-06-09 18:45:52 +0530
---

## Links 

- [Pair in C++ Standard Template Library (STL) - GeeksforGeeks](https://www.geeksforgeeks.org/pair-in-cpp-stl/)

### Summary 

> Pair is used to combine together two values that may be different in type. Pair provides a way to store two heterogeneous objects as a single unit.  

- Initialization Syntax : 
	- `pair (data_type1, data_type2) Pair_name (value1, value2)`
- Access 
	- `Pair_name.first` to get the first value, similarly second.

```cpp

// declaration
pair<int, string> p1;

// adding values
p1 = make_pair(1, "abc");
cout << p1.first << " " << p1.second; // 1 abc
p1 = {2, "xyz"};
cout << p1.first << " " << p1.second; // 2 xyz

// add with other pairs
pair<int, string> p2 = p1; // pass by val
cout << p2.first << " " << p2.second; // 2 xyz
pair<int, string> &p3 = p2; // pass by ref
p3.first = 5;
cout << p2.first << " " << p2.second; // 5 xyz

pair<int,int> p_array[3];
p_array[0]={1,2};
p_array[1]={3,4};


```



---

Return to [[CPP STL]]

---
