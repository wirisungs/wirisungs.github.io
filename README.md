# Welcome to my profile, is Wirisu here!

Hello world! My name is **Wirisu/Willis, a full-stack developer**! I'm a **21-year-old student** currently dying in deadline and stuff...

# About my carreer & my social activities
This is a list of my currently/past jobs, projects,...

## What I'm Doing
- **Last Wednesday Society Owner**: I'm working as a owner of my server named Last Wednesday Society.
- **HUTECH's IT Got talent former contestant**: IT Got Talent is a vibrant and meaningful academic competition, providing an opportunity for students from different universities to interact and learn from each other. This is not only a platform to promote scientific research movements but also a place to discover and honor outstanding young talents. The competition aims to select and train potential students to participate in academic arenas at the city, national, and international levels. At the same time, IT Got Talent serves as a bridge, supplying high-quality Information Technology human resources to meet the needs of businesses and contribute to the development of society.
- **CSGO Tournament Analysis**: CSGO Tournament Analysis is a Python project that uses CSV data to analyze, evaluate, and predict the Major champion of the first-person shooter game CS:GO.

## My social account
- **Facebook**: facebook.com/mikuislife12
- **Messenger**: m.me/mikuislife12
- **Github**: github.com/wirisungs
- **Discord**: @ng.wiris.22

# Sample code (C++)
```cpp
/*
        wirisungs.dev, a riel developer!
    */
    
    //system("cls")
    #pragma GCC optimize("O3")
    #include <bits/stdc++.h>
    // #include <ext/pb_ds/assoc_container.hpp>
    
    #define TIME (1.0 * clock() / CLOCKS_PER_SEC)
    #define tc int t = 1; cin >> t; for(int i = 1; i <= t; i++)
    #define F first
    #define S second
    #define MK make_pair
    #define PB push_back
    #define POPB pop_back
    #define POBF pop_front
    #define ins(vr, x) vr.insert(x)
    #define ers(vr, x) vr.erase(x)
    #define cnt(vr, x) vr.count(x)
    #define fnd(vr, x) vr.find(x)
    #define fndstr(s , k) s.find(k) != string :: npos;
    #define max_el(a) *max_element(all(a))
    #define all(v) begin(v), end(v)
    #define rall(v) rbegin(v), rend(v)
    #define sr(v) sort(all(v))
    #define arrsort(a, n) sort(a, a+n)
    #define rev(v) reverse(v.begin(), v.end())
    #define revarr(v, n) reverse(v, v + n)
    #define rand(v) random_shuffle(v.begin(), v.end())
    #define randarr(v, n) random_shuffle(v, v + n)
    #define vsize(a) a.size()
    #define lg(s) s.length()
    #define sqr(a) (a)*(a)
    #define ansyes "YES"
    #define ansno "NO"
    #define nl endl 
    #define opt() ios::sync_with_stdio(false); cin.tie(NULL); cout.tie(NULL);
    #define openfile(name) freopen(name".inp", "r", stdin); freopen(name".out", "w", stdout);
    #define cerrtime(time, movie, song) cerr << "Time elapsed: " << time << "s\nToday's recommend anime: " << movie << "\nNow playing: " << song << "\nCode by untrusted (a.k.a kuzeki.hitoru).\n";
    #define get(s) getline(cin >> ws, s)
    #define whl(a) while(a--)
    #define __untrusted__() int main()
    #define __akk1to__(n) void solve(int n)
    #define ffor(a) for(int i = 0; i < a; i++)
    #define ret(a) return cout << a << nl, void();
    #define ret2(a, b) return cout << a << ' ' << b << nl, void();
    #define ret3(a, b, c) return cout << a << ' ' << b << ' ' << c << nl, void();
    #define retbool(a) return cout << (a ? ansyes : ansno) << nl, void();
    #define iteaccess(v) for(auto it = v.begin(); it != v.end(); it++)
    #define rtc(n) cout << "Case #" << n << nl;
    
    #define INT_CHECK 1e5
    const int INT_SS = 1e9 + 5;
    const int MOD = 1e9 + 7;
    
    using namespace std;
    // using namespace __gnu_pbds;
    typedef long long ll;
    typedef long double ld;
    // typedef tree<int, null_type, less<int>, rb_tree_tag, tree_order_statistics_node_update> indexed_set;
    typedef string str;
    using vi = vector<int>;
    using vl = vector<ll>;
    using vii = vector<vector<int>>;
    using viit = vector<int>::iterator;
    using pii = pair<int, int>;
    using dqi = deque<int>;
    using dql = deque<ll>;
    using si = set<int>;
    using sl = set<ll>;
    using msi = multiset<int>;
    using msl = multiset<ll>;
    using sig = set<int, greater<int>>;
    using slg = set<ll, greater<ll>>;
    using siiter = set<int>::iterator; // auto it = s.begin();
    using sliter = set<ll>::iterator; // auto it = s.begin();
    using mii = map<int, int>;
    using mll = map<ll, ll>;
    using mil = map<int, ll>;
    using mli = map<ll, int>;
    using mstri = map<str, int>;
    using mstrl = map<str, ll>;
    using mistr = map<int, str>;
    using mlstr = map<ll, str>;
    
    int subarray[2009][2009];
    
    // void setin(str c){ freopen(c.c_str(), "r", "stdin"); }
    // void setout(str c){ freopen(c.c_str(), "w", "stdout")
    
    // find element nearest to x
    // auto it = s.lower_bound(x);
    // if(it == s.begin()) {
    //     cout << *it << nl;
    // } else if (it == s.end()) {
    //     it--; cout << *it << nl;
    // } else {
    //     int a = *it; it--;
    //     int b = *it;
    //     if(x - b < a - x) cout << b << nl;
    //     else cout << a << nl;
    // }
    
    // indexed_set func (work with iterator (auto)):
    // s.find_by_order(a): returns an iterator to the element at a given position
    // s.order_of_key(a): returns the pos of a given element
    
    #define maxN 1e5 + 1;
    
    
    vl createPFS(const vl &inp){
        vl psum(vsize(inp) + 1);
        partial_sum(begin(inp), end(inp), begin(psum) + 1);
        return psum;
    }
    
    vi graph[1001];
    vector<bool> ifvisit(1001, false);
    
    void DFS(int u){
        ifvisit[u] = true;
        for(auto x : graph[u]){
            if(!ifvisit[x]) DFS(x);
        }
    }
    
    // int binarysearch(vi &a, int query){
    //     int left = 0, right = lg(a) - 1;
    //     while(left < right){
    //         int m
    //     }
    // 
    
    __akk1to__(){
        
    
    __untrusted__(){
        opt();
        // tc solve(i);
        solve(1);
        cerrtime(TIME, "JJK - Seasion 2", "Curtain call - Toiki, CONA");
        return 0;
    }
```
