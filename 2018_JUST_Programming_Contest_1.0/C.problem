#include <bits/stdc++.h>
using namespace std;
#define IO ios_base::sync_with_stdio(0),cin.tie(0)
#define mem(a,b) memset(a,b,sizeof(a))
#define FIN freopen("in.txt","r",stdin)
typedef long long LL;

const int maxn = 1e6+5;

int T;
LL n, euler[maxn];


void Euler()
{
	euler[1]=1;  
	for (int i = 2; i < maxn; ++i)  
		euler[i]=i;  
	for (int i = 2; i < maxn; ++i) {  
		if (euler[i] == i) {  
	    for (int j = i; j < maxn; j+=i)  
				euler[j]=euler[j]/i*(i-1);
	  }
	}
}

int main() {
	//FIN;
	Euler();
	cin >> T;
	while (T--) {
		cin >> n;
		cout << euler[n]*(n-1) << endl;
	}
	return 0;
}