# Leetcode-Problem-Sloving-Sloutions-
#30 days challenge to slove atleast one leetcode problem every day.<br>
<b>#Day 1: 12/09/2023<br><b>
<b>Problem Statement:</b><br>
Given an integer n, return the number of trailing zeroes in n!.<br>
<B>Solution:<b><br>
First we willunderstand term trailing zeroes <br>
Trailing zeros:Trailing zeroes are a sequence of 0 in any positive representation of a number,after which no other digits follow.<br>
For example:<br>
Input: n = 5<br>
Output: 1 <br>
Factorial of 5 is 120 which has one trailing 0.<br>
Input: n = 20<br>
Output: 4<br>
Factorial of 20 is 2432902008176640000 which has<br>
4 trailing zeroes.<br>
<b>Code</b>
code:
#include <iostream>
using namespace std;
int countTrailingZeroes(int n)
{ int count = 0;
for (int i = 1; i <= n; i++) {
int j = i;
while (j % 5 == 0) {
count++;
j /= 5;
}
}
return count;
}

int main()
{ int n,x ;
do
{
cout<<"\nEnter the value of n";
cin>>n;
cout << countTrailingZeroes(n) << endl;
cout<<"\nTo continue type 1";
cin>>x;
} while(x==1);
return 0;
}




