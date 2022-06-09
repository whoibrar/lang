---
published : true

title : "CPP STL Queue"
permalink : "/cpp/stl/queue"
layout : note
excerpt : 

alias : 
categories : "cpp"
tags : 


created_at: 2022-06-09 13:25:38 +0530
modified_at: 2022-06-09 13:26:54 +0530
---

## Summary

```cpp

// FIFO
// First In First Out 

// Queue in bus stop

// Operations 

	q.push(val)		// add val to stack
	q.front()		// access the value 
	q.pop()			// removes the value
	q.empty()		// returns boolean 


queue<string> q;
q.push("abc"); q.push("def"); q.push("ghi");

while(!q.empty()){
	cout << q.front << endl;
	q.pop();
}


```
 ---

 Return to [[CPP]]

 ---
