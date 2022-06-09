---
published : true

title : "CPP STL Set Multi"
permalink : "/cpp/stl/set/multi"
layout : note
excerpt : 

alias : 
categories : "cpp"
tags : 

created_at: 2022-06-08 22:18:25 +0530
modified_at: 2022-06-08 22:25:39 +0530
---


### Summary 

- Allows duplication of keys in set
	- *you had one job 🤦*
- Can be used as an alternative to Priority Queue 


```cpp

multiset<int> s;
s.insert(3);
s.insert(1);
s.insert(2);
s.insert(3);
s.insert(2);
s.insert(4);
s.insert(5);

print(s); // 1 2 2 3 3 4 5

// deleting with key 
// deletes all keys 

s.erase(3); // removes all occurrence of 3
print(s); // 1 2 2 4 5

// deleting with iterator
// deletes only first occurence

auto itr = s.find(2);
s.erase(itr);
print(s); // 1 2 4 5



```

 ---

 Return to [[CPP]]

 ---
