---
published : true

title : "CPP Errors"
permalink : "/cpp/errors"
layout : note
excerpt : "Errors I stumbled upon"

alias : 
categories : "cpp"
tags : 

created_at: 2022-06-03 19:05:56 +0530
modified_at: 2022-06-08 21:40:36 +0530
---

### No TOH for you

[[algo.tower-of-hanoi#Abort signal from abort 3 SIGABRT]] ?



### map undeclared : first use in the function error

- [Stack Overflow ](https://stackoverflow.com/questions/20871375/map-undeclared-first-use-in-the-function-error)
	- use `std` namespace
		- `std::map` when using it 
		- `using std::map` or `using namespace std`


### error: terminate called after throwing an instance of 'std::bad_alloc'
- [Stack Overflow](https://stackoverflow.com/questions/39935786/c-error-terminate-called-after-throwing-an-instance-of-stdbad-alloc)
	- Stuff that results in Undefined Behavior 
		- Increment unspecified value

### error: non-void function does not return a value in all control paths [-Werror,-Wreturn-type]

```cpp 
int findval2(vector<int> &v){
	for(int i=0;i<v.size();i++){
		if(i==2){
			return v[i];
		}
	}
}

// error is generated because
// 

```

---

Return to [[CPP]]

---