---
published : false

title : 
permalink : 
layout : note
excerpt : 

alias : 
categories : 
tags : 

# publishedDate : 2022-05-30 00:00:00 +0000

---

### Why cant I create Subsets

- pass by reference 
- 



```cpp

#include <bits/stdc++.h>
using namespace std;

void getar(int a[], int n);
void getar(string a[], int n);
void setar(int a[], int n);
void getv(vector<int> v);
void getv(vector<string> v);

void solve(vector<int> v, int curr, int end, vector<int> out, vector<vector<int>> ans) {

	if (curr > end) {
		ans.push_back(out);
		return;
	}

	// dont
	solve(v, curr + 1, end, out, ans);

	// take
	out.push_back(v[curr]);
	solve(v, curr + 1, end, out, ans);

	return;

}

vector<vector<int>> subsets(vector<int>& v) {
	vector<vector<int>> ans;
	vector<int> out;
	solve(v, 0, v.size() - 1, out, ans);

	for (int i = 0; i < ans.size(); i++) {
		for (int j = 0; j < ans[i].size(); j++) {
			cout << ans[i][j];
		}
	}
	return ans;

}



int main() {

	vector<int> v = {1, 2, 3};
	subsets(v);

	// int n; cin >> n; int arr[n]; setar(arr, n);
}



















void getv(vector<string> v) {
	int n = v.size();
	cout << "---" << endl << "[";
	for (int i = 0; i < n - 1; i++) {
		cout << v[i] << ", ";
	}
	cout << v[n - 1] << "]" << endl << "---";
}

void getv(vector<int> v) {
	int n = v.size();
	cout << "---" << endl << "[";
	for (int i = 0; i < n - 1; i++) {
		cout << v[i] << ", ";
	}
	cout << v[n - 1] << "]" << endl << "---";
}

void getar(int a[], int n) {
	cout << "---" << endl << "[";
	for (int i = 0; i < n - 1; i++) {
		cout << a[i] << ", ";
	}
	cout << a[n - 1] << "]" << endl << "---";
}

void getar(string a[], int n) {
	cout << "---" << endl << "[";
	for (int i = 0; i < n - 1; i++) {
		cout << a[i] << ", ";
	}
	cout << a[n - 1] << "]" << endl << "---";
}

void setar(int a[], int n) {
	for (int i = 0; i < n; i++) {
		cin >> a[i] ;
	}
}

```


### Subset Sum GFG Segmentation

- Global variables declared outside of class 

- [Subset Sum Problem | Practice | GeeksforGeeks](https://practice.geeksforgeeks.org/problems/subset-sum-problem-1611555638/1/)

```cpp

// m* n where all v[m][n]=0
vector<vector<int>> v(m,vector<int>(0,n));
vector<int> dp[100];





int DP[100][100000];
bool solve(vector<int>v, int sum, int start) {
	if (sum == 0) {return true;}
	if (start > v.size()) {return false;}

	if (DP[start][sum] != -1) {return DP[start][sum];}
	else {
		bool take = solve(v, sum - v[start], start + 1);
		bool dont = solve(v, sum, start + 1);

		DP[start][sum] = (take or dont);
		return DP[start][sum];
	}

}

bool isSubsetSum(vector<int>arr, int sum){
	memset(DP, -1, sizeof(DP));
	return solve(arr,sum,0);
}

```

- Literally the same code works in Interviewbit but not in GFG
- https://www.interviewbit.com/problems/subset-sum-problem/

