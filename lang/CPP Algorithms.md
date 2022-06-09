---
published : true

title : "CPP Algorithms"
permalink : "/cpp/algo"
layout : note
excerpt : 

alias : 
categories : "cpp"
tags : 

created_at: 2022-06-09 18:42:35 +0530
modified_at: 2022-06-09 18:42:35 +0530
---

## Links

- [algorithm - C++ Reference](https://m.cplusplus.com/reference/algorithm/)

## Summary

```cpp

// time complexity 
	// most of these is O(N)

// upper lower bound
////////////////////

	// regular search

	lower_bound(n.begin(), n.end(), X) -> returns iter of 1st value that is >= X.
	upper_bound(n.begin(), n.end(), X) -> returns iter of 1st value that is > X



	// search in custom range
	lower_bound(n.begin()+5,n.end(),X) -> starts from 5th element


	// for sets and maps use this, use below syntax
	// also can't use the custom search range

	m.lower_bound(X);
	m.upper_bound(X);

	// occurence using upper_bound and lower_bound 
	// on a sorted array
	// difference of those two will be no of occurence
	cout << upper_bound(v.begin(), v.end(), val) - lower_bound(v.begin(), v.end(), val);


// min and max
//////////////
	
	// can also use custom range

	// iterator to min
	int mn_itr = min_element(v.begin(),v.end());
	// min element 
	int mn = *min_element(v.begin(),v.end());
	
	// iterator to max
	int mx_itr = max_element(v.begin(),v.end());
	// max element
	int mx = *max_element(v.begin(),v.end());

// accumulate
/////////////
	
	int intial_sum = 0; // mandatory to pass
	int sum = accumulate(v.begin(),v.end(),intial_sum);

// count
////////

	// no of occurrence of x in v in defined range
	int cnt = count(v.begin(),v.end(),x);

	// time complexity 
		// maps and sets -> O(log N)
		// vecotrs -> O(N)

// find
///////

	// returns iterator to position 
	auto it = find(v.being(),v.end(),x);

	// if empty returns v.end()



	// can be used to get index in vectors ...
	// by subtracting iterator to first

	auto it = find(v.being(),v.end(),x);
	int idx_of_x = it-v.begin();


// reverse
//////////
	
	reverse(v.begin(),v.end()); 
	
	// can pass custom range as well 

	// use this on string, arrays


// all_of // any_of // none_of
//////////////////////////////

	// syntax
	all_of(start_at, end_before, boolean_function);

	// check if all are posistive 
	// also uses lambda functions
	cout << all_of(v.begin(), v.end(), [](int x) {return x > 0;}) << endl;
	
	// same as below
	bool ispositive(int x){return x>0;}
	cout << all_of(v.begin(), v.end(), ispositive);
	
	vector<int> v{5, 4, 3, 2}; //1
	vector<int> v{1,2,3,-1}; //0

	// all_of vs any_of vs none_of 
	// all_of -> needs all to be evaluated to true
	// any_of -> single true will result in true 
	// none_of -> needs all to be evaluated to false


```

 ---

 Return to [[CPP]]

 ---