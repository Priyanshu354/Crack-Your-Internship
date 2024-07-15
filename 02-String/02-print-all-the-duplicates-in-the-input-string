#include <bits/stdc++.h>
using namespace std;

int main()
{
    string s;
    cin>>s;
    
    unordered_map<char,int> m;
    
    for(int i=0;i<s.size();i++){
        m[s[i]]++;
    }
    
    for(auto it : m){
        if(it.second > 1){
            cout << it.first << ", count" << it.second << endl;
        }
    }

    return 0;
}