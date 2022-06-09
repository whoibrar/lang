---
published : true

title : "CPP NameScope"
permalink : "/cpp/namescope"
layout : note
excerpt : 

alias : 
categories : 
tags : 

# date : 2022-03-27 00:00:00 +0000

showfooter : 
showgraph : 
created_at: 2022-06-09 21:46:55 +0530
modified_at: 2022-06-09 21:46:55 +0530
---

## Global Scope

### Why Can't I [[CPP Cout]] outside of main in Global Scope ?
- only declarations and definitions can appear at global scope.
- These definitions can include expressions.
- `int a = 5; int b=a+5;` is valid but `int a=5; int b; b=a+5` is not  

```cpp
#include <iostream>
std::cout << "outside";

int main(){
	std::cout << "inside";
}

```

### Run code before main() 
- Global variable constructors and initializers which are too complex to be executed at compile time have to run before main 
- [startup - Can C++ have code in the global scope? - Stack Overflow](https://stackoverflow.com/questions/51886189/can-c-have-code-in-the-global-scope)

```cpp

#include <bits/stdc++.h>
using namespace std;

int a = 5;
int b = a + 6;

int x = []() {
	cout << "enter num : ";
	int temp;
	cin >> temp;
	cout << temp << endl;
	return temp;
}();

int main() {
	cout << a << " " << b << endl;
}

```

---

Return to [[CPP]]

---
