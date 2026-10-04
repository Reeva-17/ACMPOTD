## Approach
Sort the array and take the minimum as a[0]. Then traverse the array from the second element and find the first element that is strictly greater than a[0]; that is the second order statistic. If no such element exists, print NO
## Code
```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    vector<int> a(n);

    for (int i = 0; i < n; i++) {
        cin >> a[i];
    }

    sort(a.begin(), a.end());

    for (int i = 1; i < n; i++) {
        if (a[i] > a[0]) {
            cout << a[i];
            return 0;
        }
    }

    cout << "NO";

    return 0;
}
```
Complexity :

Time complexity: O(n log n)

Space Complexity: O(n)

<img width="1804" height="270" alt="image" src="https://github.com/user-attachments/assets/60392e6e-943e-4c75-b134-20bfcfc53a3f" />
