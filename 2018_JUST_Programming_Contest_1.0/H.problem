#include <bits/stdc++.h>
using namespace std;
#define IO ios_base::sync_with_stdio(0),cin.tie(0)
#define mem(a,b) memset(a,b,sizeof(a))
#define FIN freopen("in.txt","r",stdin)
typedef long long LL;

const int maxn = 2e5+5;

int T, n, m, p;
string s, c;
set <int> st;

int main() {
	//FIN;
	IO;
	cin >> T;
	while (T--) {
		st.clear();
		cin >> n >> m;
		cin >> s;
		for (int i = 0; i < n; ++i) {
			if (s[i] != s[n-1-i]) {
				st.insert(i);
				st.insert(n-1-i);
			}
		}
		int ans = 0;
		while (m--) {
			cin >> p >> c;
			p--;
			s[p] = c[0];
			if (s[p] == s[n-p-1]) {
				st.erase(p);
				st.erase(n-p-1);
			}
			else {
				st.insert(p);
				st.insert(n-p-1);
				continue;
			}
			if (st.empty()) ans++;
		}
		cout << ans << endl;
	}
	return 0;
}