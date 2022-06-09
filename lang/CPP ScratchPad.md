---
published : true

title : CPP ScratchPad
permalink : /cpp/notes
layout : note
excerpt : 

alias : ["CPP ScratchPad"]
categories : 
tags : 

# date : 2022-03-27 00:00:00 +0000

showfooter : 
showgraph : 
---


```cpp

/////////////////////////
// HEADER FILE TO INCLUDE
/////////////////////////

	#include <bits/stdc++.h> 
	
	/*this imports all required for CP
	adding this costs compilation time 
	but that has no effect on TLE 
	which is the execution time*/

//////////////////////////////////////
// VARIABLE DECLARATION AND DATA TYPES
//////////////////////////////////////

	// type name = value; 
	// char, int, float, double, bool
	// long int, long long int
	
	
	int a = 4.5; // a will store 4
	cout << a  // 4
	cout << a++; // 4 
	cout << ++a; // 6
	a++; // first use then incriment
	++a; // firt incriment then use
	
	
	bool x = false;
	cout << x; // output is 0 as except zero all numbers are considered true
	
	
	char first = 'a';
	char second = 'b';
	cout << (int) first; // 97 type cast char a to get its ascii value
	cout << second-first; // 1 as the difference 
	
	char c; // say input is 9
	cin >> c; // here the ascii value of nine is stored in c
	cout << c << "<->" << (int) c; // 9<->57 as, 1st is char 9 and ascii of char 9 
	
	
	// single quotes for single characters 
	// double quotes for strings
	
	// cin works with line breaks or white spaces
	// so it can skip any if in between
	
	
	int a, b; char c;
	cin >> d >> a;  // say input is 12 345 
	cout << d << " " << a; // 1 2 as character sees the first char of digits 12 and uses 1 for itself

///////////////////////
// CHARACTER PRECEDENCE
///////////////////////

	// double > float > long long int > int > char
	// expresion is evaluated to higher data type
	
	cout << 5/2 ; //2
	cout << 5/2.0; //2.5
	
	double a = 3/2; 
	cout << a; // 1 as first 3/2 is evaluated to 1 and that value is stored in a
	cout << (double) 3/2; // 1.5 as 3,2 first converted and then evaluated 
	
	
	// for same level, go left to right
	cout << 7 / 2 * 3; //9 as its 3*3 
	cout << 3 * 7 / 2; //10 as its 21/2 
	
	// see precedence table 
	// [Operators Precedence in C](https://www.tutorialspoint.com/cprogramming/c_operators_precedence.htm)

//////////////////////
// OVERFLOW DATA TYPES 
//////////////////////

	-10^9 < int < 10^9
	-10^12 < long int < 10^12
	-10^18 < long long int < 10^18
	
	INT_MIN < int < INT_MAX
	INT_MX + 1 = INT_MIN
	
	int a = 100000
	int b = 100000
	long int c = a*b;
	cout << c;
	
	/* generally use int or long long int
	not to use double because of percision errors
	double can store large numbers at the cost of accuracy */
	
	double a = 100000;
	double b = 100000;
	double c = a * b; 
	cout << c; // 1+e10 scientific notation
	cout << fixed << c; // 10000000000.00000 prints the number
	cout << fixed << setprecision(2); //100000000000.00 only two numbers after decimal
	
	double x = 1e24; // 10^24
	cout << x; // doesn't acutally print 10 with 24 zeroes it prints 9999.. which is close to 10^24 but not exactly equal

////////////
// OPERATORS 
////////////
	&& and
	|| or

//////////
// SCOPES 
//////////

	// variables declared in scope can't be used outside
	// scope starts and ends with { }

	////////////////////////////
	// ACESSING | LOCAL | GLOBAL
	////////////////////////////

		#include<bits/stdc++.h>
		string s = "global";
		int main() {
	
		// Using Extern
		string s = "local";
		cout << "no extern : " << s << endl;       //local
	
		if (true) {
			extern string s;
			cout << "yes extern : " << s << endl; //global
			}
	
		// Scope Resolution Operator
		cout << s << endl; 	 // local
		cout << ::s << endl; //global
		}


/////////////
// SEXY LOOPS
/////////////

	// for(initialisation;condition;operation)
		for(int i; i<1=10; cout<<i++<<endl){}; // prints one to 10 in new lines

	// do something to test cases
		int t; cin >> t; while(t--){/*do something*/};

	// infinte loops 
		for(;;){};
		while(1);

	// break and continue act on previous for loop
		for(int j=0;j<10;j++)
			{
			for(int i=0;i<10;i++)
				{
				if (i==5)
					{
					if(true)
						{
						if(true)
							{
							break; //breaks out of loop 
							}
						}
					}
				}
			}


	// auto i in array
		for(auto i : arr){cout<<i<<" ";}

//////////////
// CPP STRINGS
//////////////

	//////////////////////
	// STRINGS ARE MUTABLE
	//////////////////////

		cin >> s; // input is hello
		s[0]='y'; // now its yello
		s.size(); // 5 
		getline(cin,s1); // takes till newline found, ignores space
		cin.ignore(); //forgets the new line 

	////////////////////////
	// READ LINES FROM INPUT
	////////////////////////
		
		/* INPUT
		3 
		abc def ghi
		jkl mno
		pqr stu */
		
		int t; cin>>t; cin.ignore();
		while(t--){
			string s;
			getline(cin,s);
			cout<<s<<endl;
		}

	////////////////////////////////////
	// CONCATING A CHARACTER TO A STRING 
	////////////////////////////////////

		ans_string +=str[index] // O(len(str)) [don't]
		ans_string.pushback(str[index]) // O(1) [do]

	///////////////////////////////////////////
	// DEALING WITH UNBELIEVEABLY LARGE NUMBERS
	///////////////////////////////////////////
	
		/* say you want to add 5 to 1234567890123456789088977865745340874321
		instead of converting it to a number datat type 
		store it as a string and perform the required operations
		manipulate the last_digit */
		
		string s;
		cin >> s;
		int last_digit = s[s.size() - 1] - '0' //we subtract zero to calibrate for ascii

/////////////////////
// SEGMENTATION FAULT
/////////////////////

	// It occurs when we are trying to access the part of memory which is yet to be allocated or used. 
		int n = 5;
		int arr[n]; // n be the size of the integer array
		char arr2[n] // character array of size n which is not prefered
		arr[8]; // this will lead to segmentation error
	
	// make a 2D matrix 
			/* 3 3
			1 2 3
			4 5 6 
			7 8 9 */
			int m,n;
			cin >> m >> n;
			for(int i=0;i<n;++i){
				for(int j=0;j<m;++j){
					cin>>a[i][j];
				}
			}

////////////////////
// ARRAY SIZE LIMITS
////////////////////

	////////////////////////
	// FINDING SIZE OF ARRAY
	////////////////////////
	
		// sizeof() which gives byte size
		// sizeof(arr)/sizeof(arr(0))

		// Using Pointers
		// *(&a+1) - a
			int n = 3;
			int a[n];
		
			a[0] = 5;
			a[1] = 6;
			a[2] = 7;
		
			cout << a[0] << " : " << &a[0] << endl; // 5 : 0x61fed8
			cout << a[1] << " : " << &a[1] << endl; // 6 : 0x61fedc
			cout << a[2] << " : " << &a[2] << endl; // 7 : 0x61fee0
			cout << a[3] << " : " << &a[3] << endl; // 6422224 : 0x61fee4
			cout << &a + 1 << endl;					// 0x61fee4
		
			// a[3] does't exist so garbage and next address
			// &a + 1 similarly gets the next address after the array ends
			// 



	// global arrays are initialsized to zero

	/* this depends on machine but generally
	local array can be declared upto 10^5 size 
	global array can be of 10^7 size upto
	
	why?
	cause local arrays declared are stored in stack memory
	this has a limit (~8mb) which can overflow
	but globals are in heap / text segment memory don't have this limit 
	*/
	
	const int n = 2e7; // 2*(10^7)
	int a[n]; //global array of bigger size 

//////////////////////////////////////
// WHY NO RETURN 0 IN MAIN IS OPTIONAL
//////////////////////////////////////

	// returnTypex funName (paraType1 paraVal1, paraType2 paraType2){
	// return valTypex
	// }
	
	/* The compilers of yester years needed the `reteurn 0;` statement to get
	that the code has finally finished successfully. But newer compilers auto
	assumes the `return 0;` if it does not exist.
	*/

////////////////////////////
// PASS | REFERENCES | VALUE
////////////////////////////

	////////////////
	// PASS BY VALUE
	////////////////
	
		void incriment(int n){n++;} 
		int main(){
			int a = 3;
			cout << a << endl; // 3
			incriment(a);      // copy of the original value a is passed
			cout << a << endl; // 3 as there is no change 
		}

	////////////////////
	// PASS BY REFERENCE
	////////////////////
	
		// (&n) is refernce of variable (n)  
		// don't actually need to know pointers

		void incriment(int &n){n++;}
		int main(){
			int a = 3;
			cout << a << endl; // 3
			incriment(&a);     // reference to orginial value a is passed
			cout << a << endl; // 4 as the value is changed in incirment function
		}
	

	////////////////////////////////
	// SWAP NUMBERS USING REFERENCES
	////////////////////////////////
	
		void swap(int &a, int &b){int temp = a; a = b; b = temp;}
		int main(){
			int a = 3;
			int b = 5;
			cout << a << " " << b << endl; // 3 5 
			swap(a,b);                     // gets swaped by the function
			cout << a << " " << b << endl; // 5 3 
		}

	/////////////////////
	// POINTERS IN ARRAYS
	/////////////////////

	// Arrays are always paseed by reference
		void func(int a[]){a[0]=5;} //don't need to declare the size 
		int main(){
			int a[2]; 
			a[0]=3;
			cout << a[0] << endl; // 3
			func(a);              // passed by reference to func 
			cout << a[0] << endl; // 5 
		}

	// need to define Di for i>1 i.e, 2D's, 3D's, etc 
		void func(int a[][5]){/*do thing*/} // a[][5] a[][5][5] etc


	// how not to pass 2D arrays to functions
		void func(int n, int m, int a[][m]){a[0][0]=5} 
		int main(){
			int n=3,m=3;
			int a[n][m];
			a[0][0]=7;
			cout << a[0][0] << endl;
			func(n,m,a[][m]);
			cout << a[0][0] << endl;
		}

	// declare 2D arrays globally 
	
		// instead of main to avoid passing into func 
		// okay for Competitive but not in actual Development
		// this saves time and effort
		const int N = 1e3;
		int a[N][N];
		void func(){a[0][0]=1;}
		int main(){
			a[0][0]=7;
			cout << a[0][0] << endl;
			func();
			cout << a[0][0] << endl;
		}

/////////
// ERRORS
/////////

	/* RTE can occur at recursion instead of TLE
	this happens when the stack memory exceeds and the data overflows
	similarly Recurrsion can lead to MLE */

//////////////////
// TIME COMPLEXITY
//////////////////
	
	/*10^7 iterations(operations) can be performed in one second
	*/

/////////////////////
// MODULAR ARITHEMTIC
/////////////////////

	// why is it answer % (10^9 + 7)
		// its very close to int max value
		// so final ans can be stored as int
		// its a prime number
		// so multiplicate inverse can be found easily

	/////////////////
	// MODULO FORMULA
	/////////////////
	
		// if a<b => a%b = a
		// ...(((a)%m)%m)%m... => a%m [as (a%m) will be < m]
		
		// (a+b)%m => ( (a%m) + (b%m))%m
		// (a*b)%m => ( (a%m) * (b%m))%m
		// (a-b)%m => ( (a%m) - (b%m) + m)%m
		// (a/b)%m => ( (a%m) * mutli_inverse(b)%m )%m

	///////////////////
	// FACTORIAL MODULO
	///////////////////

		// we need to find factorial mod M
		// instead of finding factorial and then Mod M
		// simply apply the modulo prop to use
		
		for(int i=2;i<=n;++i){fact1=fact1*i;} cout<<fact1%M; 
		// can be written as 
		for(int i=2;i<=n;++i){fact2=(fact2*i)%M;} cout<<fact2;

		// why this works 
		// (1*2*3*4*5)%M
		// (1*2*3*4)%M * (5)%M)%M
		// ( ( (1*2*3)%M * (4)%M )%M ) * (5)%M)%M 	

///////////
// POINTERS 
///////////

	// 8bits = 1byte 
	// Adress of byte when prited gives HexaDecimal
	
	int x; // say 4bytes are allocated for saving x
	x = 4; 
	cout << &x; // gives address of x
	
	// this address can't be directly stored
	// so pointer was created to store this address
	
	int *p_x; // declaring pointer to store address of x
	p_x = &x  //this stores the adress of integer x in p_x
	
	cout << *p_x;  // value at adress in p_x
	*p_x += 1;     // change val at address by p_x to 5
	p_x +=1 ;      // moves to next block depending of type of variable declared and memory used.
	

	/////////////////////////////////////////////
	// ... pointer of reference of pointer of ...
	/////////////////////////////////////////////
	
		// ...(value at(address of(value at (address(...)))))...
		
		int a = 5;
		cout << a << endl; 			// 5
		cout << (&a) << endl;		// 0x61ff0c
		cout << *(&a) << endl;		// 5
		cout << &(*(&a)) << endl;	// 0x61ff0c
		cout << *(&(*(&a))) << endl;// 5

	//////////////////
	// Double Pointers 
	//////////////////

		int x = 4;
		int *p_x;
		int **p_p_x;
	
		p_x = &x;
		p_p_x = &p_x;
	
		cout << x << endl; //4
		cout << &x << endl; //hex1
		cout << p_x << endl; //hex1
		cout << *p_x << endl; //4
		cout << p_p_x << endl; //hex2
		cout << *p_p_x << endl; //hex1
		cout << **p_p_x << endl; //4


	/////////////////////
	// POINTERS IN ARRAYS
	/////////////////////
	
		int b[3];
		b[0] = 6;
		b[1] = 7;
		b[2] = 8;
		
		cout << b << endl;    //0x61ff04
		cout << &b << endl;   //0x61ff04
		cout << *(&b) << endl;//0x61ff04
		
		cout << b[0] << endl;    //6
		cout << &b[0] << endl;   //0x61ff04
		cout << *(&b[0]) << endl;//6	
		
		cout << (b + 1) << endl; //0x61ff08
		cout << *(b + 1) << endl;//7
		cout << (b[1]) << endl;  //7
		cout << &(b[1]) << endl; //0x61ff08
	
		// array name is pointer to the 1st memory location  
		// b == &b == &b[0] 
			
		// next pointer is next memory allocation 
		// b+1 == &(b[1])
		// this is 4 greater (next val jumps to 4) 
		// 0x61ff04 -> 0x61ff08
		// because size of int is 4

	/////////////////////////////
	// INCRIMENT POINTER FUNCTION
	/////////////////////////////

		void inc(int *x){ (*x)++;}
		int main(){
			int a = 4;
			cout << a << endl;
			inc(&a);
			cout << a << endl;
		}

////////////////////////////
// PRECOMPUTATION TECHNIQUES
////////////////////////////

	// Factorial Example

		// instead of calculating from 1 everytime
		// use the precalculated values by storing them in an data-structure
		long long int fact = 1;
		for(int i=2;i<=n;i++){fact=fact*i;}
			
		const int n = 1e5; long long fact[n];
		for(int i=2;i<=n;i++){fact[i]=fact[i-1]*i;}
		// second for loop saves time

	// return the count of given numbers
		// given input of array of size N 10^5
		// given Q queries 10^5
		// return count for each query in array

		// instead of creating array first
		// ..later counting for each element 
		// ..this gives O(N*Q) > 10^10

		// use global array to directly store
		// ..count values when input is taken
		// ..this gives O(N) < 10^5

	// Hashing Negative elements 

		// Precomputation works on setting the values but we start with zero
		// ..for negatvie add most negative 
		// ..the resulting will positive
		// ..subtract appropriate for indexing

	// Prefix Sum
	
		// Using global array cause that initialize with zero
		// ..Use one based indexing to avoid adding if/else
		// ..whlist using index start and end

	

```


---

Return [[CPP]]

---
