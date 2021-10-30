# 💼 CodeChef SRM KTR Chapter 
![cclogo](https://user-images.githubusercontent.com/75165587/139527897-bf8e691b-8421-4d7b-ba8c-bcaba945cc75.png)

## 👧 Applicant Name : CHETAS SHREE MADHUSUDHAN 
### 📋 Onboard 2021 
### 📋 Phase 2 
## 💻 Task for CP domain (Task for 2nd year students)
# 📂 Task 1: Spot the error in following questions: 
## 📍 Answer 1:

```C
#include <stdio.h> 
int main() 
{ 
int number, LD; 
printf(" Enter a number"); 
scanf("%d", &number); //user should put input here 
LD = number % 10; 
printf(" \n The Last Digit of a Given Number %d = %d", number, LD); return 0; 
} 
```
## 📍 Answer 2:

```C
int sumcal(int len, int* arr, int value) 
{ 
int sum = 0; 
for(int i =0 ; i< len-1; i++ ) 
{ 
if(arr[i]%value == 0) 
sum =+ arr[i]; 
} 
return sum; 
}
```
## 📍 Answer 3:

```C
#include <stdio.h> 
int main() 
{ 
for(int i=1;i <= 4;i++) 
{ 
for(int j=1;j <= 4; j++) 
{ 
if(i != j) 
{ 
printf("*"); 
} 
else 
{ 
printf(" "); 
} 
} 
printf("\n"); 
} 
return 0; 
} 
```
## 📍 Answer 4:

```C
#include <stdio.h> 
void main() { 
char a='A'; 
a>10?printf("Yes"):printf("No"); 
}
```
## 📍 Answer 5:

```C++
#include <iostream> 
using namespace std; 
int main() { 
int o, i, s; 
for(o=5; o>=1; o--) 
{ 
for(s=1; s<=5-o; s++) 
cout<<" "; 
for (i=1; i<=o; i++){ 
cout<<"*";} 
cout<<endl; 
}}
```
## 📍 Answer 6:

```
z=int(“Enter a number:”) 
for in range [0,9]: 
if z==x: 
print(“They are equal”); 
else: 
print(“They are not equal”); 
```
## 📍 Answer 7:

```C++
#include <iostream> 
using namespace std;
class test{ 
	public:
	int my_variable; 
};
int main() { 
test code_chef; 
int x;
cin>>x;
code_chef.my_variable=x; 
if(code_chef.my_variable%2==0){ cout<<"Even"; 
} 
else{ 
cout<<"odd"; 
} 
return 0; 
}
```

## 📍 Answer 8:

```C++
#include <iostream>
using namespace std;
void printSums(int N)
{
	int start = 1, end = (N + 1) / 2;
	while (start < end)
	{
		int sum = 0;
		for (int i = start; i <= end; i++)
		{
			sum = +i;
			if (sum == N)
			{
				for (int j = start; j <= i; j++){
					cout << j << " ";
				cout << "/n";
				break;
			}
			if (sum > N)
				break;
		}
		sum = 0;
		start++;
	}
}
}
int main()
{
	int n;
	cin >> n;
	printSums(n);
	return 0;
}
```
## 📍 Answer 9:

```C++
#include <iostream> 
using namespace std; 
int main() { 
int length;
cout<<"enter the length of the array"<<endl;
cin>>length; 
int array[length]; 
for(int i=0;i<length;i++){ 
cin>>array[i]; 
} 
int min=array[0];
int max=array[0]; 
for(int i=1;i<length;i++){ 
if(array[i]>max) 
max = array[i]; 
else if(array[i]<<min) 
min = array[i]; 
} 
cout<< min<<" "<<max; 
return 0; 
} 

```
## 📍 Answer 10:

```C
#include <stdio.h> 
#include <string.h> 
main() 
{ 
int t,i,diff_count; 
scanf("%d",&t); 
char s[100001]; 
while(t--){ 
diff_count=0; 
scanf("%s",s); 
for(int i=0;i<strlen(s)-1;i++){ 
if(s[i]==s[i+1])
diff_count++; 
} 
printf("%d\n",diff_count); 
return 0; 
} 

```


# 📂 Task 2: Solve the given programs: 
## 📍 Question 1: 

Given a group of words, rearrange them in alphabetical order on the basis of their fourth alphabet. Take the last letter into consideration if the word contains less than 4 characters. Minimum word length would be of two characters. 
```C++
    #include <bits/stdc++.h>
    using namespace std;
    int main(){
        int n;
        cin>>n;
        string s1;
        char s2;		
        priority_queue<pair<char,string>,vector<pair<char,string>>,greater<pair<char,string>>> min;
        for(int i=0;i<n;i++){
            cin>>s1;
            if(s1.length()>=4) s2 = s1[3];
            else s2 = s1[s1.length()-1];
            min.push({s2,s1});
        }
        while(!min.empty()){
            cout<<min.top().second<<endl;
            min.pop();
        }
        return 0;
    }

```
## 📍 Question 2: 

Given an array arr[] and an integer K where K is smaller than the size of the array, the task is to find the Kth smallest element in the given array. It is given that all array elements are distinct. Check if kth element is a prime number or not. 

```C++ 
    #include <bits/stdc++.h>
    using namespace std;
    bool check_prime(int n){
        for(int i=2;i*i<n;i++){
            if(n%i==0) return false;
        }return true;
    }
    int k_small_num(int arr[],int k,int n){
        priority_queue<int>max;
        for(int i=0;i<n;i++){
            max.push(arr[i]);
            if(max.size()>k){
                max.pop();
            }
        }
        return max.top();	
    }
    int main(){
        int n,k;
        cin>>n>>k;
        int arr[n];
        for(int i=0;i<n;i++) cin>>arr[i];
        int x = k_small_num(arr,k,n);
        cout<<"The "<<k<<"th smallest element is the array is "<<x<<" and it is ";
        if(check_prime(x)) cout<<"a prime number.";
        else cout<<"not a prime number.";
        return 0;
    }
```
## 📍 Question 3:

Rajesh is a 5 year old kid who is practising the alphabet. He is really confused with the homework he has got and he needs your help to do the homework. The homework is to print alternate letters from A to Z in alternate uppercase and lowercase.

```C++
    #include <bits/stdc++.h>
    using namespace std;
    int main(){
        char arr[] = {'A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','W','X','Y','Z','a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z'};
        int i=0;
        int st1 = 0;
        int st2 = 28;
        while(i!=13){
            if(i%2==0){
                cout<<arr[st1];
                st1+=4;			
            }else{
                cout<<arr[st2];
                st2+=4;			
            }
            cout<<"\n";
            i++;
        }
        return 0;
    }
```

## 📍 Question 4:

Given a number n, find out whether this number is Chef number or not.Let's consider an example of 297 as a Chef number: square of 297 is 88209; divided it into two portions, 88 and 209; now total them, 88 + 209 to get 297 back. Consider an n-digit number k (take another example of 45). Square it (452 = 2025) and add the right n digits (that is 25) to the 
remaining n or n-1 digits (in this case, 20). If the resultant quantity is k, then k is a Chef number (45 is a Chef number as 20 + 25 = 45). Splitting of the squared number should be based on the number of digits of the given number.

```C++
    #include <bits/stdc++.h>
    using namespace std;
    int len_num(int n){
        int len=1;
        if (n > 0) {    
        for (len = 0; n > 0; len++) {
            n /= 10;
            }
        }return len;
    }
    bool chef_num(int n){
        int x = n*n;	
        int l = len_num(x);
        int y = l/2;
        int u = 10;		
        while(y--){
            u*=10;
        }	  
        int e1 = x/u;
        int e2 = x%u;	
        return (e1+e2 == n) ?  true : false ;
    }
    int main(){
        int n;
        cin>>n;
        if(chef_num(n)){
            cout<<"Chef Number ";
        }else{
            cout<<"Not Chef Number";
        }
        return 0;
    }

```
