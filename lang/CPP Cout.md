---
published : true

title : "CPP cout"
permalink : "/cpp/cout"
layout : note
excerpt : "Standard output CPP"

alias : ["cout","std::cout"]
categories : 
tags : 

# date : 2022-03-27 00:00:00 +0000

showfooter : 
showgraph : 
---
### Links 

- [C++ cout - C++ Standard Library](https://www.programiz.com/cpp-programming/library-function/iostream/cout)

### std::cout [[vs]] cout 

- `std::cout` is used when not `using namespace std` in code.

```cpp
#incldue <iostream>
int main(){
	std::cout<< "without namspace";
}

#incldue <iostream>
using namespace std;
int main(){
	cout<<"with using";
}
```

### `cout` Member functions

```cpp

// cout Member functions
cout.put(char c)  // display char type c stored by variable
cout.put(65)  // A
cout.put('x') // x 


cout.write(char *str, int n) // display first n from str
cout.write("hello world")    // hello


cout.precison(int n) //shows upto n digits 
cout << setpricison(n) 

```

### The What ?

- cout object used to display output to std output device, its defined in [[iostream]]
- The **"c"** in `cout` refers to **"character"** and **"out"** means **"output"**. Hence `cout` means **"character output"**. 
- The `cout` object in C++ is an object of class `ostream`. It is associated with the standard C output stream `stdout`.
- declared in `std::cout` inside `<iostream>`

---

Return to [[CPP]]

---
