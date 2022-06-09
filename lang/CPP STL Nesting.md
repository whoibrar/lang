---
published : true

title : "CPP STL Nesting"
permalink : "/cpp/stl/nesting"
layout : note
excerpt : 

alias : 
categories : "cpp"
tags : 

created_at: 2022-06-09 18:44:20 +0530
modified_at: 2022-06-09 18:45:52 +0530
---

## Summary

```cpp

// sample data structure to store 
// firstname lastname and marks 


int main() {
	map<pair<string, string>, vector<int>> m;
	int n; cin >> n;

	for (int i = 0; i < n; i++) {
		// firstname lastname count of vector size
		string fn, ln; int cnt; cin >> fn >> ln >> cnt;

		// create corresponding vector for pair in m
		m[ {fn, ln}];

		// adding values to vector
		for (int j = 0; j < cnt; j++) {
			int temp; cin >> temp;
			m[ {fn, ln} ].push_back(temp);
		}
	}

	// printing the values
	for (auto val : m) {

		
		// name is a pair of fn and ln
		auto name = val.first; 
		cout << name.first << " " << name.second << endl;

		// list is vector 
		auto list = val.second;

		for (auto i : list) {
			cout << i << " ";
		}
		cout << endl;
	}
}

// input 
// 3 
// abc bcd 3
// 1 2 3
// abc bce 1
// 3
// abb def 2
// 6 7


// output 
// abb def
// 6 7 
// abc bcd
// 1 2 3 
// abc bce
// 3 


```

---

Return to [[CPP STL]]

---
