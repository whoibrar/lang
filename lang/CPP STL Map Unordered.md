---
published : true

title : "CPP STL Unordered Map"
permalink : "/cpp/stl/map/unordered"
layout : note
excerpt : 

alias : 
categories : "cpp"
tags : 

# date : 2022-05-17 00:00:00 +0000

created_at: 2022-06-08 19:53:57 +0530
modified_at: 2022-06-09 18:47:22 +0530
---

## Links 

- [C++ HashMaps - Lei Mao's Log Book](https://leimao.github.io/blog/CPP-HashMaps/)
- [unordered_map in C++ STL - GeeksforGeeks](https://www.geeksforgeeks.org/unordered_map-in-cpp-stl/)

## Summary 

- Stores elements formed by key-value and mapped value.
	- Internally implemented using Hash Table
	- Key value is used to uniquely identify elements. 
	- Mapped value is content associated with key.
- Time Cost is depends on hashing function, but is generally O(1) for search, insert and delete.

### `unordered_map` [[vs]] `unordered_set`
- unordered_set only has keys, which can be used for checking presence.
- unordered_map also has values, which can be used for checking frequency.


### [[CPP STL Map]] [[vs]] [[CPP STL Map Unordered]]
- Ordering 
- Implementation 
	- `map` ->  Red Black Trees
	- `unordered_map` -> Hash Table
- Time Complexities 
	- map  `~O(log n)`
	- unordered_map `~O(1)`
- Valid Key Types
	- Maps use comparison so they are can use complex data structures as well.
	- OM Can only use those which has hash function defined
		- Works 
			- int, float, double, string ... etc
		- Doesn't work
			-  sets, vectors, set of sets ... etc
			- cause pair dosen't have any pre-built hash function

## Code Snippet

```cpp 

// Unordered_map 101
////////////////////

	// Declaration 
	//////////////

	unordered_map<string, int> um;

	// adding
	/////////

	um["alpha"] = 1;
	um.insert(make_pair("beta", 2));

	// finding
	//////////

	// if not found, iterator to end is returned
	// if found, iterator to it is returned

	bool x = (um.find("alpha") != um.end());
	// if above true, then found

	// printing
	///////////

	unordered_map<string, int>:: iterator itr;
	for (itr = um.begin(); itr != um.end(); itr++) {
		cout << (itr->first) << " : " << (itr->second) << endl;
	}



```


 ---

 Return to [[CPP]]

 ---
