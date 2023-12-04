#include<bits/stdc++.h>
using namespace std;
#define forn(i, n) for (int i = 0; i < int(n); i++)
#define ll long long
const int N = 1e5;
vector<int>g[N];
int vis[N];
int level[N];
void bfs(int source){
    queue<int>q;
    q.push(source);
    vis[source] = 1;
   
    while(!q.empty()){
        int cur_v = q.front();
        q.pop();
        cout << cur_v << " ";
        for(int child : g[cur_v]){
            if(!vis[child]){
                q.push(child);
                vis[child] = 1;
                level[child] = level[cur_v] + 1;
            }
        }
    }
    
    cout << endl;
}
int32_t main() {
ios_base::sync_with_stdio(0);
cin.tie(0);

int v, e;
cin >> v >> e;

while(e--){
    int x, y;
    cin >> x >> y;

    g[x].push_back(y);
    g[y].push_back(x);
}

bfs(1);

for(int i = 1; i <= v; i++){
    cout << i << ":" << level[i] << endl;
}
 
return 0;
}
