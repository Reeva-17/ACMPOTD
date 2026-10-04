## Approach
Sort the soldier's heights and use two pointers to find how many soldiers can pair with each soldier such that their height difference is at most d. Count each valid pair twice because (i,j) and (j,i) are different. 
## Code
```cpp
#include <bits/stdc++.h>
using namespace std;
 
int main() {
    int n;
    long long d;
    cin >> n >> d;
 
    vector<long long> a(n);
 
    for (int i = 0; i < n; i++) {
        cin >> a[i];
    }
 
    int ans = 0;
 
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if (i != j && abs(a[i] - a[j]) <= d) {
                ans++;
            }
        }
    }
 
    cout << ans;
 
    return 0;
}
```
Complexity:

Time Complexity: O(n²)

Space Complexity: O(n)

<img width="1813" height="299" alt="image" src="https://github.com/user-attachments/assets/56e16025-693c-4101-86ad-2bd169c3e704" />
