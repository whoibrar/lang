---
published : true

title : "CPP STL Set"
permalink : "/cpp/stl/set"
layout : note
excerpt : 

alias : 
categories : "cpp"
tags : 

# date : 2022-05-16 00:00:00 +0000


created_at: 2022-06-08 21:28:28 +0530
modified_at: 2022-06-09 18:36:45 +0530
---

## Links 

- [Set in C++ Standard Template Library (STL) - GeeksforGeeks](https://www.geeksforgeeks.org/set-in-cpp-stl/)

### Summary 

- Declaration Syntax 
	- `set<datatype> setname;`
	- `set<int> s = {-1,2,3,0}`
- Properties 
	- Sorted
	- Unique 
	- Immutable
	- [[Red Black Trees]]
	- Un-indexed
- Time Complexity `~O(log N)`
	- insertion
	- erase 
	- count 
	- Clear `O(N)`

```cpp


// Set 101
//////////

int n[] = {1, 2, 3, -1, -2, -3, 0};

// intialization
////////////////

	set<int> s1;
	set<int, greater<int> > s2;

// adding elements
//////////////////

	for (int i = 0; i < sizeof(n) / sizeof(n[0]); i++) {
		s1.insert(n[i]);
		s2.insert(n[i] * 5);
	}

	set<int> mySet(s1.begin(), s1.end());
	mySet.insert(s2.begin(), s2.end());


// print elements
/////////////////


	for (auto i : mySet) {
		cout << i << " ";
	}

	// s1 ==> -3 -2 -1 0 1 2 3
	// s2 ==> 15 10 5 0 -5 -10 -15
	// mySet ==> -15 -10 -5 -3 -2 -1 0 1 2 3 5 10 15

// check if element exists in set
/////////////////////////////////

	// if found returns iterator to it
	// if not found returs iterator to end.
	auto it = mySet.find(-2);

	// if ture then element exists
	it != mySet.end();

	// 1 if persent, 0 if not
	cout << mySet.count(25);

// upper lower bounds
/////////////////////

	// lower bound ==> equivalent or not go before it
	// upper bound ==> firt element that will go after it

	cout << *mySet.lower_bound(10) ; // 10
	cout << *mySet.upper_bound(10) ; // 15

// union and intersection
/////////////////////////

	set<int> squares = { 1, 4, 9, 16, 25 };
	set<int> even = { 2, 4, 16, 6 };

	set<int> allnum(squares);
	allnum.insert(even.begin(), even.end());
	// 1 2 4 6 9 16 25

	set<int> even_squares;
	set_intersection(squares.begin(), squares.end(), even.begin(), even.end(), inserter(even_squares, even_squares.begin()));
	// 4 16

```

 ---

 Return to [[CPP]]

 ---
