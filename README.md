# Minimum-delete-operations-to-make-all-elements-of-array-same
C++

** PROBLEM STATEMENT**

Given an array of n elements such that elements may repeat. We can delete any number of elements from the array. The task is to find a minimum number of elements to be deleted from the array to make it equal.
Examples:

Input: arr[] = {4, 3, 4, 4, 2, 4}

Output: 2

After deleting 2 and 3 from array, array becomes 
arr[] = {4, 4, 4, 4} 

Input: arr[] = {1, 2, 3, 4, 5}

Output: 4
We can delete any four elements from array.

**CODE**

Time complexity:O(N)

```

#include <bits/stdc++.h>

using namespace std;

int main()
{
   int n;
    cin>>n;
    int a[n];
    for(int i=0;i<n;i++)
    {
cin>>a[i];
}
   unordered_map<int,int>mp;
    for(int i=0;i<n;i++)
    {
        mp[a[i]]++;
    }
    int max_ct=0;
    for(auto i:mp)
    {
        if(i.second>max_ct)
        {
            max_ct=i.second;
        }
    }
    
    cout<<n-max_ct;

    return 0;
}
