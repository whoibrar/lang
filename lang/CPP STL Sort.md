---
published : true

title : "CPP STL Sort"
permalink : "/cpp/stl/sort"
layout : note
excerpt : 

alias : 
categories : "cpp"
tags : 

created_at: 2022-06-09 14:55:03 +0530
modified_at: 2022-06-09 18:45:52 +0530
---

## CPP STL Sort 
-  Implementation 
	- using three different sorting algorithms
	- Starts with Quick Sort
	- Switches to Heap Sort
	- If less elements then Insertion Sort
- 

```cpp

// sorting 101
//////////////


	sort(start_from, end_before);

	int arr[]; // say size n
	sort(arr, arr+n);

	vector<int> v;
	sort(v.begin(),v.end());

// How any swapping works 
/////////////////////////


	// here the swapping depends on the 
	// condition inside the if

	vector<int> v {5, 4, 2, 3, 1};
	int n = v.size();
	for (int i = 0; i < n; i++) {
		for (int j = i + 1; j < n; j++) {
			//this is comparion part
			if (v[i] > v[j]) { 
				swap(v[i], v[j]);
			}
		}
	}
	
	// increasing order
	if(v[i]>v[j]){
		swap(v[i],v[j]);
	}

	// decreasing order
	if(v[i]<v[j]){
		swap(v[i],v[j]);
	}

	// above can be abstracted to external function
	// now we define a custom function 
	
	if(doswap(v[i],v[j])){
		swap(v[i],v[j]);
	}
	bool doswap(int a, int b) {
		return a < b;  // swaps decending
		return a > b;  // swaps ascending
	}

// custom sorting comparator 
///////////////////////////
	
	// first term ascending 
	// second term descending 

	bool doswap(pair<int, int> a, pair<int, int> b) {
		if (a.first != b.first) {
			if (a.first > b.first) {return true;}
		}
		else {
			if (a.second < b.second) {return true;}
		}

	}

	int main() {
		{% raw %}
		vector<pair<int, int>> v{{5, 4}, {5, 5}, {1, 2}, {1, 5}};
		{% endraw %}
		int n = v.size();
		for (int i = 0; i < n; i++) {
			for (int j = i + 1; j < n; j++) {
				if (doswap(v[i], v[j])) {
					swap(v[i], v[j]);
				}
			}
		}
		for (auto i : v) {
			cout << i.first << " " << i.second << endl;
		}
	}

	// output 
	// 1 5
	// 1 2
	// 5 5
	// 5 4


// passing the custom comparator function
/////////////////////////////////////////
	
	// it should be defined in such a way that 
	// when swapping should be done it should return false 


	// write what you need 
	// as in if you need a < b 
	// simply write return a<b in comparator function

	
	bool doswap(pair<int, int> a, pair<int, int> b) {
		if (a.first != b.first) {
			return a.first < b.first;
		}
		else {
			return a.second > b.second;
		}

	}
	
	// here in the final ans we need a.first < b.first 
	// and also a.second > b.second 

	

```


--- 

Return to [[CPP STL]]

---
