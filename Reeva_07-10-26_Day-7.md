## Approach

Start from rank a and move up to rank b. Add the years required for every promotion from a to b.
So, sum all d[i] where a <= i < b.

## Code
```cpp
#include <bits/stdc++.h>
using namespace std;
 
int main() {
    int n;
    cin >> n;
 
    vector<int> d(n);
 
    for (int i = 1; i < n; i++) {
        cin >> d[i];
    }
 
    int a, b;
    cin >> a >> b;
 
    int ans = 0;
 
    for (int i = a; i < b; i++) {
        ans += d[i];
    }
 
    cout << ans << endl;
 
    return 0;
}
```
Complexity:

Time Complexity: O(n)

Space Complexity: O(n)

<img width="1807" height="456" alt="image" src="https://github.com/user-attachments/assets/90a8a374-6320-4010-9f75-edcea6c3a50a" />
