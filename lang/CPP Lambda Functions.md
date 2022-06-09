---
published : true

title : "CPP Lambda functions"
permalink : "/cpp/func/lambda"
layout : note
excerpt : 

alias : 
categories : "cpp"
tags : 

created_at: 2022-06-09 16:40:10 +0530
modified_at: 2022-06-09 16:43:24 +0530
---

### Read more 

- [Lambda expression in C++ - GeeksforGeeks](https://www.geeksforgeeks.org/lambda-expression-in-c/)
- [Lambda expressions in C++ - Microsoft Docs](https://docs.microsoft.com/en-us/cpp/cpp/lambda-expressions-in-cpp?view=msvc-170)

### Summary 

```cpp
// lambda function 101
//////////////////////

	// regular function 
	int plusone(int x) {
	return x + 1;
	}
	
	// lambda function
	[](int x){return x+1}();
	
	// comparision 
	int val = 5;
	cout << plusone(val); 
	cout << [](int x) {return x + 1;}(val);


	// replace every number by its square in vector
	vector<int> v{5, 4, 3, 2};
	for (int i = 0; i < v.size(); i++) {
		v[i] = [](int x) {return x * x;}(v[i]);
	}
	

	// naming lambda functions 
	auto square = [](int x) {return x * x;};
	vector<int> v{5, 4, 3, 2};
	for (int i = 0; i < v.size(); i++) {
		v[i] = square(v[i]);
	}
	// 25 26 9 4

```


 ---

 Return to [[CPP]]

 ---
