---
published : true

title : "CPP STL Iterators"
permalink : "/cpp/stl/iterators"
layout : note
excerpt : 

alias : 
categories : "cpp"
tags : 

created_at: 2022-06-08 18:50:31 +0530
modified_at: 2022-06-09 00:03:59 +0530
---


```cpp

// Iterators 101
////////////////

	vector<int> v{1, 3, 5};
	vector<int> :: iterator itr;
	itr = v.begin();
	
	cout << itr; // error 
	cout << *itr; // 1


	// iterator for vector of pair of int and int
	{% raw %}vector<pair<int, int>> vp = {{1,2},{2,3},{3,4}};{% endraw %}
	vector<pair<int,int>> :: iterator itr;

	for(itr = vp.begin(); itr!=vp.end();itr++){
		cout << (*itr).first << " " << itr->second << endl;
	}

	// itr->first is same as (*itr).first

	// begin()
	// pointes to  beginning 
	
	// end()
	// points to element after end 

// Iterator to last element
///////////////////////////

	auto last_itr = --myContainer.end();

// itr++ vs itr+1
//////////////////

	// itr++ points to next iteration
	// itr+1 points to next location 
		// works in vecotrs
		// doesnt work in maps and sets 

// Range based loops 
////////////////////

	vector<int> v = {1,2,3,4,5};
	
	// values are copied to i
	// 1 2 3 4 5
	for(int i : v){
		cout << i << " "; 
	}
	
	// reference is copied to i
	// 2 3 4 5 6
	for(int &i : v){
		i++;
		cout << i << " ";
	}
	
// auto keyword 
///////////////

	{% raw %}
	vector<pair<int, int>> vp = {{1, 2}, {2, 3}, {3, 4}};
	{% endraw %}
	for (auto itr = vp.begin(); itr != vp.end(); itr++) {
		cout << (*itr).first << " " << itr->second << endl;
	}	

	// this combines auto with range based loops 
	for(auto &value: vp){
		cout << value.first << " " << value.second << endl;
	}

```

 ---

 Return to [[CPP]]

 ---
