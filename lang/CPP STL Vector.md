---
published : true

title : "CPP STL Vector"
permalink : "/cpp/stl/vector"
layout : note
excerpt : 

alias : 
categories : "cpp"
tags : 

# date : 2022-05-31 00:00:00 +0000


created_at: 2022-06-03 17:41:21 +0530
modified_at: 2022-06-08 18:18:55 +0530
---

```cpp

// Intialization
////////////////

	// empty vector
	vector<int> v;

	// vector of size n
	vector<int> v(10); 

	// 1-D of size n and all values as 0
	vector<int> vec(n, 0);  

	// 2-D of size rows x col and all values as 0
	vector<vector<int>> vec(rows, vector<int>(col, 0)); 

	// with values 
	vector<int> nums1 = {3, 1, 4, 1, 5};
	vector<int> nums2 {6, 9, 69, 96};

	// from array
	int arr[] = {5,10,15,20};
	int n = sizeof(arr)/sizeof(arr[0]);
	vector<int> v(arr,arr+n);

	// from vector
	vector<int> x {2,3,5,7,11};
	vecotr<int> v = x; // O(N) -> copy values 
	vector<int> y(x.begin(),x.end());


	// filling a val
	vector<int> v(100);
	fill(v.begin(),v.end(),42);

// Basic Functions
//////////////////

	// get the size -> O(1)
	v.size(); 

	// check empty returns bool
	v.empty();

	// get first element
	v[0];
	v.front();

	// get last element
	*v.rbegin();
	*(v.end() - 1);
	*(v.size()-1);
	v.back();
	
	// sort 
	sort(v.begin(),v.end());
	sort(v.begin(),v.end(),greater<int>()); // decending
	
	// push_back() ands at end
		vector<int> v(5);
		print(v); // 0 0 0 0 0 
		v.size(); // 5
		v.push_back(1);
		print(v); // 0 0 0 0 0 1
		v.size(); // 6 
	
	// pop_back() removes last elemnent
		v.pop_back(); // 1

	// void print(vector<int> v); 
	// copies the vector -> O(N)

	// void print(vector<int> &v);
	// only the refernce -> O(1)

// Limitations on size, similar as arrays
///////////////////////////////////////// 

	// these limits are not because of array 
	// but because of limits on
	// function continuous memory location
	// locally declared 10^5
	// globally declared 10^7

// begin()-end() vs front()-back()
	// first two return iterator
	// last two return reference

	
// Nesting in Vectors
/////////////////////

	vector<pair<int,int>> v;
	v.push_back({1,2});
	v.push_back(makepair(3,4));

	// Array of Vectors
	///////////////////

	vector<int> v[3]; 
	// no of rows is fixed (3) 
	// no of cols is dynamic 

	v[0] = {1, 2, 3};
	v[1] = {4, 5, 6};
	v[2] = {7, 8, 9};
	getv(v[0]); // 1 2 3
	getv(v[1]); // 4 5 6
	getv(v[2]); // 7 8 9


```

---

 Return to [[CPP]]

---
