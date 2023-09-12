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
<b>Code</b><br>
#include &lt;iostream&gt;<br>
using namespace std;<br>
 
int countTrailingZeroes(int n)<br>
{<br>
    int count = 0;<br>
    for (int i = 1; i <= n; i++) {<br>
        int j = i;<br>
        while (j % 5 == 0) {<br>
            count++;<br>
            j /= 5;<br>
        }<br>
    }<br>
    return count;<br>
}<br>
int main()<br>
{
    int n,x ;<br>
    do<br>
    {<br>
    cout<<"\nEnter the value of n";<br>
    cin>>n;<br>
    cout << countTrailingZeroes(n) << endl;<br>
    cout<<"\nTo continue type 1";<br>
    cin>>x;<br>
} while(x==1);<br>
    return 0;<br>
}





