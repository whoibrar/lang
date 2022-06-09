---
published : true

title : "CPP STL Stack"
permalink : "/cpp/stl/stack"
layout : note
excerpt : 

alias : 
categories : "cpp"
tags : 

created_at: 2022-06-09 13:27:11 +0530
modified_at: 2022-06-09 13:27:11 +0530
---

## Summary

```cpp

// LIFO
// Last In First Out 

// Stack of plates

// Operations 

	st.push(val)	// add val to stack
	st.top()		// access the value 
	st.pop()		// removes the value
	st.empty()		// returns boolean 

stack<int> s;
s.push(2); s.push(3); s.push(4); s.push(5);

while(!s.empty()){
	cout << s.top() << endl;
	s.pop();
}

```

---

 Return to [[CPP]]

---
