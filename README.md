readme-edits
# hello-world-again
I'd written this code for the techgig goddess competition. Only one test case was successfully tested. 
The code requires you to give the maximum characters occuring in the string. The number of strings have to be inputted by the user. Following are the limits.
1<=number of strings inputted<=10
The string can have upto 100000 characters.
Any changes, corrections or improvements are welcome.

# techgig
WELLLLL
#include <bits/stdc++.h> 
using namespace std; 
  
// function to find the maximum occurring character in 
// an input string which is lexicographically first 
char getMaxOccurringChar(char str[]) 
{   
    // freq[] used as hash table 
    int freq[26] = { 0 }; 
  
    // to store maximum frequency 
    int max = -1; 
  
    // to store the maximum occurring character 
    char result; 
  
    // length of 'str' 
    int len = strlen(str); 
  
    // get frequency of each character of 'str' 
    for (int i = 0; i < len; i++) 
        freq[str[i] - 'a']++; 
  
    // for each character, where character is obtained by 
    // (i + 'a') check whether it is the maximum character 
    // so far and accordingly update 'result' 
    for (int i = 0; i < 26; i++) 
        if (max < freq[i]) { 
            max = freq[i]; 
            result = (char)(i + 'a'); 
        } 
  
    // maximum occurring character 
    return result; 
} 
  
// Driver Code 
int main() 
{ 
    int t;
    cin>>t;
    if(t<10){
    for(int k=1;k<=t;k++){
    char str[100000];
    cin>>str;
    cout<< getMaxOccurringChar(str);
    cout<<"\n";
    }
    }
    return 0; 
    }
master
