# maps-in-c-hackerank-
Given  names and phone numbers, assemble a phone book that maps friends' names to their respective phone numbers. You will then be given an unknown number of names to query your phone book for. For each queried, print the associated entry from your phone book on a new line in the form name=phoneNumber; if an entry for  is not found, print Not found instead.
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include <map>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
    int n;
    string name;
    int pnumber;
    map<string,int> mp;
    
    cin>>n;
    for(int i=0;i<n;i++){
        cin>>name;
        cin>>pnumber;
        mp.insert(pair<string,int>(name,pnumber));
    }
    while(n>0){
        cin>>name;
            if (mp.count(name) != 0)
                cout<<mp.find(name)->first<<"="<<mp.find(name)->second<<endl;
            else
                cout<<"Not found"<<endl;
        n--;
    }
    return 0;
}
