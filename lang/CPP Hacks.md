---
published : true

title : "CPP Hacks"
permalink : /cpp/hacks
layout : note
excerpt : "Stuff that makes it easy"

alias : 
categories : 
tags : 

# date : 2022-03-27 00:00:00 +0000

created_at: 2022-06-09 21:46:38 +0530
modified_at: 2022-06-09 21:46:38 +0530
---


### Infinite Loop - Avoid TLE
[How to prevent Infinite loop in Sublime Text (Solution). - Codeforces](https://codeforces.com/blog/entry/65048)

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    ios::sync_with_stdio(0);
    cin.tie(0);
    
    while (true) {
        cout << "Hello World\n";
    }
    
}
```

---

Return to [[CPP]]

---
