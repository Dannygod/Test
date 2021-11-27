#include <iostream>
#include <bits/stdc++.h>
using namespace std;

int main()
{
    pair <int,int> p[1000];
    set<int> s;
    int i,n=3,l;
    cin>>n>>l;
    p[0].first=2,p[0].second=2;
    p[1].first=3,p[1].second=1;
    p[2].first=5,p[2].second=3;
    for(i=0;i<n;i++)
    {
        swap(p[i].first,p[i].second);
    }
    sort(p,p+n);
    for(i=0;i<n;i++)
    {
        cout<<p[i].first<<" "<<p[i].second<<endl;
    }

    s.insert(0);
    s.insert(1);
    s.insert(p[0].second);

    for(auto it=s.begin();it!=s.end();it++)
    {
        cout <<*it<<" ";
    }
    cout<<endl;
    auto it=s.find(p[0].second);
    cout<<*it<<endl;

    cout <<*next(it)<<endl;
    cout <<*prev(it)<<endl;
    cout <<*next(it)-*prev(it)<<endl;

    //set <int>s={5,2,3,6,4,3,9};

    /*set <int>s={5,2,3,6,4,3,9};//大到小

    cout <<s.count(12)<<endl;//False
    cout <<s.count(5)<<endl;//True

    //auto it=s.find (2);
    //cout <<*it<<endl;

    s.insert(7);
    s.erase(2);

    for(auto it=s.begin();it!=s.end();it++)
    {
        cout <<*it<<" ";
    }

    auto it=s.find (6);
    cout <<*it<<endl;
    cout <<*next(it)<<endl;
    cout <<*prev(it)<<endl;*/
    return 0;
}
