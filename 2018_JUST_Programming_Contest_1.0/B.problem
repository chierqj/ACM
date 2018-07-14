#include <bits/stdc++.h>
using namespace std;
#define IO ios_base::sync_with_stdio(0),cin.tie(0)
#define mem(a,b) memset(a,b,sizeof(a))
#define FIN freopen("in.txt","r",stdin)
typedef long long LL;

const int maxn = 2e5+5;

int T;
LL n, a;

bool judge (LL x, LL num) {
	LL tmp = (n-x+n-1)*x/2;
	return tmp >= num;
}

int main() {
	//FIN;
	IO;
	cin >> T;
	while (T--) {
		cin >> n >> a;
		LL x = n*(n+1)/2;
		if (x <= n*a) cout << n << endl;
		else {
			LL tmp = x-n*a;
			LL p = n-1;
			int ans = 0;
			LL low = 0, high = n;
			while (low <= high) {
				LL md = (low+high)>>1;
				if (judge(md, tmp)) {
					ans = md;
					high = md-1;
				}
				else low = md+1;
			}
			cout << n-ans << endl;
		}
	}
	return 0;
}