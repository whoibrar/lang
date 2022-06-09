---
published : true

title : "CPP STL Map"
permalink : "/cpp/stl/map"
layout : note
excerpt : 

alias : 
categories : "cpp"
tags : 

# date : 2022-05-27 00:00:00 +0000

showfooter : 
showgraph : 
created_at: 2022-06-08 18:58:33 +0530
modified_at: 2022-06-09 18:45:52 +0530
---

## Links 

- [What is the C++ STL map? - Educative.io](https://www.educative.io/edpresso/what-is-the-cpp-stl-map)


### Summary

- Stored key value pairs in ordered and sorted form
- Implemented using [[Red Black Trees]]

### Code Snippet

```cpp

// maps 101
///////////

	// declaring map
	map<int, int> sq;
	
	// check if empty
	cout << sq.empty() << endl; //1
	
	// adding values of i, i*i as key,value
	for (int i = 5; i > 0; --i) {
		sq[i] = i * i;
	}

	// declaring iterator
	map<int, int>::iterator itr;
	
	
	// iterating through map
	for (itr = sq.begin(); itr != sq.end(); itr++) {
		cout << itr->first << " : " << itr->second << endl;
	}
	// printing the key, values
	// 1 : 1
	// 2 : 4
	// 3 : 9
	// 4 : 16
	// 5 : 25
	
	// getting the size
	// 5
	cout << sq.size();
	
	// remove key-value
	// pass key to be removed
	sq.erase(3);
	
	// search
	sq.find(3)!=end(); // found 
	
	// get val at key
	sq.at(4); // returns val of key

// Time Complexity 
//////////////////

	// Insert -> O(log N)
	// Search -> O(log N)
	// Accessing -> O(log N)
	// Delete -> O(log N )

	m[3];
	// just wirting the above line will cost O(log N) time

	// it will also depend on the key type
	// as the keys get compared 
	// a long string as key will take more time than int

		map<string,string> m;
		string key = "abcdefg"
		m[key]= "zyx";
		// here it will depend on key size as well 
		// O(log N) now it will be O(key.size() * log N)

// Adding Elements 
//////////////////
	map<int, string> m;
	m[1] = "abc";
	m.makepair({2,"def"});](<map%3Cint, string%3E m;
	m[1] = "abc";
	m.insert({2, "def"});
	m.insert(make_pair(3, "ghi"));
	m[4];

	for (auto &i : m) {
		cout << i.first << " " << i.second << endl;
	}
	// 1 abc
	// 2 def
	// 3 ghi
	// 4

// Accessing Non Existing Elements 
	m[5]; 
	// say key 5 doesn't already exist
	// adds corresponding value for key 
	// for int val, zero is added 
	// for string, empty string is added 
	// for vector, empty vector is added
	// ... so on

// adding repetive keys, vals 
	// will overried old val with new 

// finding
//////////

	auto it = m.find(3);
	if (it==m.end()){
		// value not found
	}
	else{
		// key is itr->first
		// val is itr->second
	}

// erasing
//////////

	// using key
	// if not persent no change
	m.erase(3);

	// using iterator
	auto i = m.find(4);
	m.erase(i);

		// if the value is not persent
		// will give segementation fault 
	


```


---

Return to [[CPP STL]]

---
